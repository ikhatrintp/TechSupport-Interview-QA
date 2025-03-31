# Email Protocols and Concepts

This document covers key email protocols, their functionalities, and related concepts.

## 1. Main Email Protocols

**Q: What are the main email protocols used for sending and receiving emails?**  
**A:** The main email protocols are:
- **SMTP** (Simple Mail Transfer Protocol) for sending emails
- **POP3** (Post Office Protocol version 3) and **IMAP** (Internet Message Access Protocol) for receiving emails

## 2. SMTP Protocol

**Q: Can you explain how SMTP works?**  
**A:** SMTP is used to send emails from a client to a mail server or between mail servers. The process involves:
1. Client connects to the SMTP server
2. Authenticates if required
3. Sends the email
4. SMTP server forwards email to recipient's mail server

**Ports:**
- Port 25 (default)
- Port 465 (historically for SMTP over SSL/TLS)
- Port 587 (preferred for secure transmission)

## 3. POP3 vs IMAP

**Q: What is the difference between POP3 and IMAP?**  
**A:**

| Feature | POP3 | IMAP |
|---------|------|------|
| Email Storage | Downloads to client device | Keeps on server |
| Multi-device | Not ideal | Perfect for multiple devices |
| Ports | 110 (unencrypted), 995 (SSL/TLS) | 143 (unencrypted), 993 (SSL/TLS) |

## 4. IMAP Functionality

**Q: How does IMAP work?**  
**A:** IMAP:
- Keeps emails on server
- Syncs across multiple devices
- Downloads headers first, full messages when needed
- Real-time management of emails

## 5. Email Relay

**Q: What is an email relay, and how does it work?**  
**A:** Email relay is the process of forwarding an email from one server to another until it reaches its final destination, using SMTP.

## 6. SMTP Relay Security

**Q: What is a "relay" in SMTP, and why can it be a security concern?**  
**A:** SMTP relay forwards emails between servers. Open relays (accepting emails from any sender) can be exploited by spammers.

## 7. TLS in Email

**Q: What is TLS and why is it important in email communication?**  
**A:** TLS (Transport Layer Security) encrypts email communications, protecting sensitive information from interception.

## 8. MX Records

**Q: What are MX records, and how do they relate to email delivery?**  
**A:** MX (Mail Exchange) records specify which mail servers should receive emails for a domain.

## 9. Email Authentication

**Q: What is the purpose of SPF, DKIM, and DMARC?**  
**A:**
- **SPF**: Specifies authorized sending IP addresses
- **DKIM**: Adds digital signature to verify email authenticity
- **DMARC**: Defines policies for handling authentication failures

## 10. Email Troubleshooting

**Q: How would you troubleshoot email delivery issues?**  
**A:**
1. Verify email was sent
2. Check MX records
3. Inspect mail server status
4. Examine spam filters
5. Verify firewall settings
6. Check mailbox storage

## 11. Server Downtime

**Q: What happens if the recipient's mail server is down?**  
**A:** The sending server will retry for a period. If unsuccessful, the email bounces back with an NDR.

## 12. Non-Delivery Reports

**Q: What is an NDR and what does it contain?**  
**A:** NDR (Non-Delivery Report) is a bounce message containing:
- Error reason
- Time of attempt
- Original email/headers

## 13. Greylisting

**Q: What is Greylisting?**  
**A:** Temporarily rejects emails from unknown senders. Legitimate servers retry; many spammers don't.

## 14. Email Encryption

**Q: How does email encryption work?**  
**A:** Two main types:
1. Transport Layer Encryption (TLS) - secures connection
2. End-to-End Encryption (PGP/S/MIME) - encrypts content

## Common Email Ports

| Protocol | Port | Description |
|----------|------|-------------|
| SMTP | 25 | Default server-to-server |
| SMTP | 587 | Secure submission (preferred) |
| SMTP | 465 | Legacy SSL/TLS |
| POP3 | 110 | Unencrypted |
| POP3 | 995 | SSL/TLS |
| IMAP | 143 | Unencrypted |
| IMAP | 993 | SSL/TLS |
| HTTPS | 443 | Webmail/Exchange services |
