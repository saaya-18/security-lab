# Personal Rules of Engagement

**Name:** SAAYA SAJAN
**Date:** October 25, 2026

## 1. Authorization Statement
I own and control the environment described below. I authorize security testing only against the systems listed in the Target section.

## 2. Target (in scope)
- **System:** OWASP Juice Shop (intentionally vulnerable practice app), latest Docker image `bkimminich/juice-shop`
- **Address:** http://127.0.0.1:3000 (localhost only)
- **Host:** My own Windows laptop, running in a Docker container (WSL 2 backend)
- **Container start command:** `docker run -d --name juice-shop -p 127.0.0.1:3000:3000 bkimminich/juice-shop`

## 3. Allowed Techniques
Against the target above only:
- SQL injection
- Cross-site scripting (XSS)
- Authentication and access-control bypass testing
- Directory and endpoint enumeration
- Manual testing with a browser and its developer tools
- Intercepting my own traffic with a local proxy (for example OWASP ZAP or Burp Community)

## 4. Exclusions (out of scope)
- Any website, server, device, network or account I do not own or control
- My home router, other devices on my network, and public IP addresses
- Cloud services, university systems, and any real-world applications
- Denial-of-service or resource-exhaustion attacks against my own host
- Anything that sends test traffic outside my laptop

## 5. Network Isolation
The container port is bound to 127.0.0.1 only, so the app is reachable only from this laptop and not from other devices or the internet.

## 6. Stop Conditions
I will stop testing immediately if:
- The target becomes reachable from outside my laptop
- Any test traffic appears to leave the lab (for example, toward other hosts)
- I come across real personal data or credentials that are not part of the practice app
- The laptop becomes unstable or unresponsive
- I am unsure whether an action is within scope

To shut the lab down: `docker rm -f juice-shop`

## 7. Reporting
Any findings will be recorded with the date, the URL tested, the technique used, and the result, and will be kept only in this repository.

## 8. Signature
Signed: SAAYA SAJAN
Date: October 25, 2026
