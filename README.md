# CTF Wireshark Challenges

This repository contains two Wireshark packet capture files (`.pcapng`) related to CTF challenges. The goal is to analyze these captures to solve the following problems:

---

## Challenges

### 1. Find the Attacker's IP in a DoS Attack

- **File:** `find the find attacker's IP from where dos attack is happening.pcapng`
- **Objective:** Identify the IP address from where the Denial of Service (DoS) attack originates.
- **Hints:**
  - Look for a high volume of repeated requests or unusual traffic patterns.
  - Filter by suspicious protocols or packets flooding the target.
  - Common Wireshark filters: `ip.src`, `tcp`, `udp`, or protocol-specific filters.
  - Analyze packet timestamps and traffic distribution.

### 2. Find the Correct FTP Password

- **File:** `find the correct ftp password.pcapng`
- **Objective:** Extract the FTP login credentials (username and password) by inspecting the FTP session.
- **Hints:**
  - Use the filter `ftp` or `tcp.port == 21` to isolate FTP packets.
  - Look for `USER` and `PASS` commands in the FTP protocol.
  - Credentials are typically sent in cleartext in FTP (unless FTPS).
  - Use the "Follow TCP Stream" feature in Wireshark for easier analysis.

---

## How to Solve

1. **Open the capture file in Wireshark.**

2. **Apply the relevant filters to narrow down traffic.**

3. **For the DoS attack:**
   - Observe which IP is sending a suspiciously high number of packets.
   - Check for repetitive requests or flood patterns.
   - Identify the source IP and note it down.

4. **For the FTP password:**
   - Filter for FTP traffic.
   - Look for login commands.
   - Extract the username and password from the packet details or TCP stream.

---

## Tools Required

- [Wireshark](https://www.wireshark.org/) — Network protocol analyzer.

---

## Submission

Once you find the answers:

- For the DoS attack, provide the attacker's IP address.
- For the FTP capture, provide the username and password found.

---

Feel free to raise issues or pull requests if you want to contribute or improve this repository!
