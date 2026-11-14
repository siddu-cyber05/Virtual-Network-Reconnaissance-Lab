# Virtual Network Reconnaissance and Security Assessment Lab

## 1. Project Overview
A practical cybersecurity lab using Kali Linux and a local Python HTTP server.

## 2. Scope
Target: 127.0.0.1
Port tested: 8000
Environment: Localhost only
Tool: Nmap, curl, Python HTTP server

## 3. Tests Performed

### Nmap Scan
Command: nmap -sV -p 8000 127.0.0.1
Result: Port 8000/tcp open, HTTP service detected.

### HTTP GET
Result: HTTP 200 OK. Homepage content was returned successfully.

### HTTP HEAD
Result: HTTP 200 OK. Response headers were returned.

### HTTP OPTIONS
Result: HTTP 501 Unsupported method.
Observation: The server does not implement this HTTP method.

### robots.txt
Result: HTTP 404 File Not Found.
Observation: No robots.txt file was present.

### Server Information
The response disclosed SimpleHTTP/0.6 and Python 3.14.7.

## 4. Findings
1. Port 8000 is open on localhost.
2. The server reveals its software name and version in the HTTP Server header.
3. OPTIONS is not implemented.
4. robots.txt is absent.

## 5. Security Assessment
These tests did not confirm an exploitable vulnerability.
The server is bound to 127.0.0.1, so it is accessible only from the local machine.
The software version disclosure is informational and should not be treated as proof of compromise.

## 6. Recommendations
- Do not use Python's development HTTP server for production hosting.
- Avoid exposing unnecessary server information.
- Use a properly configured production web server for real deployments.
- Continue testing only systems you own or have permission to assess.

## 7. Conclusion
Basic local reconnaissance and HTTP security checks were completed.
Evidence was saved in the results directory.
