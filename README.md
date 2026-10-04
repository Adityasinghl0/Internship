# Task 1: Foundation & Environment Setup

## 🎯 Objective
Build strong fundamentals in cybersecurity, networking, and cryptography, and set up a professional hacking lab environment[cite: 6].

## 💻 1. Lab Environment Setup
* **Attacker Machine:** Kali Linux running on VMware[cite: 6].
* **Target Machine:** Metasploitable2 / DVWA[cite: 6].
* **Network Configuration:** Configured on a private lab network (Host-Only / NAT)[cite: 6].
  
<img width="1916" height="1022" alt="Screenshot 2026-10-04 195015" src="https://github.com/user-attachments/assets/fe21ab18-29d9-4d5c-9d75-5f0d664a9d60" />
1.1 Kali Setup
  
  <img width="1921" height="1024" alt="Screenshot 2026-10-04 195134" src="https://github.com/user-attachments/assets/ff17c4a8-256a-41c7-b972-ead3d32d7b91" />
1.2 Metasploitable2 Setup

---

## 🛡️ 2. Cybersecurity Fundamentals (CIA Triad)
* **Confidentiality:** Preventing unauthorized access to sensitive information[cite: 6]. Demonstrated using AES-256 encryption.
* **Integrity:** Ensuring data has not been altered or tampered with[cite: 6]. Demonstrated using MD5 and SHA-256 hashing.
* **Availability:** Ensuring systems and data are accessible to authorized users when needed[cite: 6].

## 🐧 3. Linux & Networking Cheat-Sheet
### File System & Permissions
* `pwd`: Print the current working directory[cite: 6].
* `ls -la`: List all files (including hidden) and their permissions[cite: 6].
* `cd <directory>`: Change directory to navigate the file system[cite: 6].
* `chmod 600 <file>`: Modify file permissions to grant read/write access to the owner only[cite: 6].
* `chown`: Change file owner and group[cite: 6].

### Networking Commands
* `ifconfig` / `ip a`: View network interface configurations and IP addresses[cite: 6].
* `ping <IP>`: Send ICMP echo requests to test network reachability[cite: 6].
* `netstat -tuln`: Display active listening ports and connections[cite: 6].

## 🔐 4. Cryptography Hands-On
* **Hashing:** Generated hashes to verify data integrity[cite: 6, 7].
  * `md5sum filename.txt`
  * `sha256sum filename.txt`
* **Symmetric Encryption:** Used OpenSSL to encrypt and decrypt a file[cite: 6, 7].
  * *Encrypt:* `openssl enc -aes-256-cbc -salt -in file.txt -out secret.enc -k password -pbkdf2`
  * *Decrypt:* `openssl enc -d -aes-256-cbc -in secret.enc -out decrypted.txt -k password -pbkdf2`

<img width="781" height="294" alt="Screenshot 2026-10-04 194602" src="https://github.com/user-attachments/assets/4ed61972-9ae6-468e-b2bc-db2fee8be846" />

## 🛠️ 5. Tool Familiarization
### Nmap (Network Scanner)
Performed a fast port scan on the local machine to identify open ports and services[cite: 7].
* `nmap -F 127.0.0.1`

<img width="581" height="160" alt="Screenshot 2026-10-04 194434" src="https://github.com/user-attachments/assets/7735aeae-51e1-42a2-a550-c081c1d178c0" />

### Wireshark (Packet Capture)
Captured and analyzed live network traffic on the `eth0` interface[cite: 7]. 
* Filtered for `icmp` traffic to isolate Ping requests and replies[cite: 7].

<img width="1670" height="875" alt="Screenshot 2026-10-04 194358" src="https://github.com/user-attachments/assets/95f40602-a93b-4466-ae3e-9e76d0d0704e" />
