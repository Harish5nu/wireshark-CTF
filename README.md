# Ethical Hacking Assignment

This repository contains a collection of practical tasks related to ethical hacking. These tasks demonstrate the use of various tools and techniques for analyzing network traffic, decrypting encoded messages, and extracting sensitive data.

---

## 📁 Assignment Tasks

### 1. DoS Attack – Source IP Identification

- **Tool Used:** Wireshark  
- **Objective:** Identify the attacker’s IP address from a DoS attack capture file.
- **File Analyzed:** `find attacker's IP from where dos attack is happening.pcapng`
- **Method:**
  - Opened the capture file in Wireshark.
  - Applied the filter: `tcp.flags.syn == 1 and tcp.flags.ack == 0`
  - Observed a SYN flood indicating a DoS attack.
- **Result:**
  - **Attacker IP (Source):** `10.20.30.40`
  - **Victim IP (Destination):** `192.168.100.128`
  - **Type of Attack:** TCP SYN Flood

---

### 2. FTP Password Extraction

- **Tool Used:** Wireshark  
- **Objective:** Extract valid FTP credentials from captured network traffic.
- **File Analyzed:** `find the correct ftp password.pcapng`
- **Method:**
  - Applied filter: `ftp`
  - Observed login attempts with various credentials.
  - Detected a successful login.
- **Successful Login:**
  - **Username:** `administrator`
  - **Password:** `nepal@123`
  - **Client IP:** `192.168.124.135`
  - **Server IP:** `192.168.124.132`

---

### 3. Base64 Decoding of Instruction File

- **Encoding Type:** Base64  
- **Tool Used:** Online Base64 Decoder  
- **Input:** `solve-me-first.txt` (Base64 encoded)  
- **Method:**
  - Decoded file using online Base64 decoder.
  - Revealed instructions for decryption tasks including RC4 and BCTextEncoder.

---

### 4. RC4 Decryption of Hexadecimal Data

- **Encryption Algorithm:** RC4 (Rivest Cipher 4)
- **Tool Used:** CrypTool  
- **Input File:** `decrypt-me.hex`
- **Key:** `5151`  
- **Method:**
  - Used CrypTool to decrypt hexadecimal data using RC4 with the provided key.
- **Result:** Decrypted plaintext revealing sensitive bank information.

---

### 5. BCTextEncoder Decryption

- **Tool Used:** BCTextEncoder Utility  
- **Input File:** `decode-me.TXT`  
- **Password:**  `k|h8@2+&P.`69L` 
- **Method:**
  - Used BCTextEncoder with the password to decode the encrypted message.
- **Result:** Successfully extracted personal information.

---

## ✅ Conclusion

This project enhanced practical cybersecurity skills through:
- Traffic analysis using Wireshark
- Decryption using CrypTool and BCTextEncoder
- Base64 decoding techniques

Each task contributed to a deeper understanding of how network vulnerabilities can be analyzed and exploited in ethical hacking scenarios.

---
