# Cybersecurity Internship – Task 1

## 🎯 Objective
Perform a TCP SYN scan on the local network to identify open ports and assess network security exposure.

## 🛠 Tools Used
- Nmap (on Linux)
- Optional: Wireshark

## 📡 Network Range Scanned
`192.168.100.0/24`

## 🔍 Devices Found and Ports

| IP Address      | Open Ports               | Services              | Risk Level |
|------------------|--------------------------|------------------------|------------|
| 192.168.100.1    | 23, 53, 80               | Telnet, DNS, HTTP      | ⚠️ High |
| 192.168.100.3    | 139, 445                 | Samba (SMB)            | ⚠️ Medium |
| 192.168.100.4    | 21, 22, 80               | FTP, SSH, HTTP         | ⚠️ Medium |
| 192.168.100.8    | 80, 135, 139, 445, 3389  | Samba, RDP (xrdp)      | ⚠️ Medium |

## 🔒 Risk Assessment & Mitigation

- **Telnet (Port 23)**: Insecure, should be disabled or replaced with SSH.
- **FTP (Port 21)**: Replace with SFTP or FTPS for secure file transfer.
- **Samba/SMB (Ports 139/445)**: Restrict to LAN and require authentication.
- **RDP (Port 3389)**: Use firewall rules to limit access and enable 2FA.
- **Unnecessary services**: Disable if not in use.

## 📸 Screenshots
Screenshots of the scan results are in the `/screenshots` folder.

## ✅ Outcome
Learned how to:
- Use Nmap for port scanning
- Identify open ports and assess services
- Recognize basic vulnerabilities in a local network
