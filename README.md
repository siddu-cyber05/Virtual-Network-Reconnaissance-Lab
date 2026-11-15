# Virtual Network Reconnaissance and Security Assessment Lab

## 1. Project Overview

A hands-on cybersecurity project built using Kali Linux to practise network reconnaissance and basic HTTP security testing in a controlled local environment.

## 2. Environment

| Component | Details |
|---|---|
| Operating System | Kali Linux |
| Target | 127.0.0.1 |
| Service | Python HTTP Server |
| Port | 8000 |
| Environment | Localhost |

## 3. Tools Used

- Nmap
- cURL
- Python 3
- Kali Linux

## 4. Practical Tasks Performed

### Network Reconnaissance
Command:
`nmap -sV -p 8000 127.0.0.1`

Result: Port 8000/tcp was found open, with an HTTP service detected.

### HTTP GET Testing
Result: HTTP 200 OK. The homepage content was returned successfully.

### HTTP HEAD Testing
Result: HTTP 200 OK. Response headers were returned.

### HTTP OPTIONS Testing
Result: HTTP 501 Unsupported method.

### robots.txt Testing
Result: HTTP 404 File Not Found.

### HTTP Header Analysis
The server disclosed:
`SimpleHTTP/0.6 Python/3.14.7`

## 5. Security Findings

1. Port 8000 was open on localhost.
2. The HTTP server disclosed software information.
3. The OPTIONS method was not implemented.
4. No robots.txt file was present.

## 6. Recommendations

- Avoid using Python's development server for production hosting.
- Minimise unnecessary server information disclosure.
- Use a properly configured production web server.
- Perform security testing only on systems you own or have permission to assess.

## 7. Project Structure

- `reports/` - Security assessment report
- `results/` - Nmap and HTTP test outputs
- `screenshots/` - Practical evidence screenshots
- `web-test/` - Local test website

## 8. Skills Practised

- Network reconnaissance
- Port scanning and service detection
- HTTP request and response analysis
- Basic security assessment
- Technical documentation
- Kali Linux command-line practice

## 9. Conclusion

This project provided practical experience with network reconnaissance and basic HTTP security testing.

All tests were performed against a local service at 127.0.0.1. No third-party systems were targeted.

The tests did not confirm an exploitable vulnerability.
