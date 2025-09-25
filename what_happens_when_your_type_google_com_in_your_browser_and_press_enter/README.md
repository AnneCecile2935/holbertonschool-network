# What Happens When You Type google.com?

*A Technical Deep Dive into Web Request Flow*

![Project Status](https://img.shields.io/badge/status-completed-success)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 📌 Project Overview

This project explains the complete journey of a web request when a user types `https://www.google.com` in their browser. Created as part of the Holberton School curriculum, it includes:

- A technical blog post explaining each step of the process
- A Mermaid diagram visualizing the flow
- All required elements for the assignment

---


---

## 🎯 Requirements Covered

| Requirement          | Implementation Location               |
|----------------------|----------------------------------------|
| DNS request          | Blog post §1 + Diagram step 1          |
| TCP/IP               | Blog post §2 + Diagram steps 2-4       |
| Firewall             | Blog post §3 + Diagram step 5          |
| HTTPS/SSL            | Blog post §4 + Diagram step 6          |
| Load-balancer        | Blog post §5 + Diagram step 7          |
| Web server           | Blog post §6 + Diagram step 8          |
| Application server   | Blog post §7 + Diagram step 8          |
| Database             | Blog post §8 + Diagram step 9          |

---

## 📄 Blog Post Content

The `article.md` file contains a complete blog post with:

1. **DNS Resolution**: Domain to IP translation
2. **TCP/IP Handshake**: Connection establishment
3. **Firewall**: Security layer
4. **HTTPS/SSL**: Encryption
5. **Load Balancer**: Traffic distribution
6. **Web Server**: Static files
7. **Application Server**: Dynamic content
8. **Database**: Data storage

**Key Features**:
- Technical explanations without jargon
- Real-world analogies
- Practical examples
- Ready for Medium/LinkedIn publication

[Read the full article →](./article.md)

---

## 🖼️ Mermaid Diagram

### Source Code (`google-request.mmd`)

```mermaid
flowchart TD
    A[You Laptop] -->|"1. What's google.com's IP?"| B[DNS Cloud]
    B --> C[Your Computer]
    C -->|"2. SYN"| D[Google Server Port 443]
    D -->|SYN-ACK| C
    C -->|ACK| D
    D -->|"3. Request"| E[Firewall]
    E -->|"4. Secure Connection"| F[HTTPS/SSL Encryption]
    F -->|"5. Encrypted Request"| G[Load Balancer]
    G -->|"6. Route to Server"| H[Application Server]
    H -->|"7. Query Data"| I[Database]
    I -->|Return Data| H
    H -->|"8. Page loads!"| A


📜 License
Distributed under the MIT License. See LICENSE for more information.
