Here’s a **complete Nmap workflow document** you can use in Kali Linux for CEH practice. It covers the phases, options, and most common commands — all in one place for copy‑paste use.

---

# 📘 Nmap Workflow & Commands (Kali Linux)

## 1. Basic Host Discovery
Check which hosts are alive.
```bash
nmap -sn 192.168.1.0/24      # Ping scan (discover live hosts)
nmap -Pn 192.168.1.10        # Treat host as up, skip ping
```

---

## 2. Port Scanning
Identify open, closed, or filtered ports.
```bash
nmap 192.168.1.10            # Default 1000 ports
nmap -p 80,443 192.168.1.10  # Specific ports
nmap -p- 192.168.1.10        # All 65535 ports
nmap -F 192.168.1.10         # Fast scan (top 100 ports)
```

---

## 3. Service & Version Detection
Find what services are running and their versions.
```bash
nmap -sV 192.168.1.10        # Detect service versions
nmap -sV --version-intensity 9 192.168.1.10   # Aggressive version detection
```

---

## 4. OS Detection
Identify operating system and device type.
```bash
nmap -O 192.168.1.10         # OS detection
nmap -A 192.168.1.10         # Aggressive scan (OS + services + scripts)
```

---

## 5. Scan Techniques
Different methods to bypass firewalls/IDS.
```bash
nmap -sS 192.168.1.10        # SYN scan (stealth)
nmap -sT 192.168.1.10        # TCP connect scan
nmap -sU 192.168.1.10        # UDP scan
nmap -sA 192.168.1.10        # ACK scan (firewall rules)
nmap -sN 192.168.1.10        # Null scan
nmap -sX 192.168.1.10        # Xmas scan
```

---

## 6. Timing & Performance
Control speed and stealth.
```bash
nmap -T0 192.168.1.10        # Paranoid (very slow, stealthy)
nmap -T4 192.168.1.10        # Faster scan (default for many)
nmap -T5 192.168.1.10        # Insane speed (noisy)
```

---

## 7. Output Options
Save results for reporting.
```bash
nmap -oN scan.txt 192.168.1.10   # Normal output
nmap -oX scan.xml 192.168.1.10   # XML output
nmap -oG scan.grep 192.168.1.10  # Greppable output
```

---

## 8. NSE (Nmap Scripting Engine)
Run scripts for deeper analysis.
```bash
nmap --script=vuln 192.168.1.10   # Run vulnerability scripts
nmap --script=http-enum 192.168.1.10   # Enumerate web directories
nmap --script=ftp-anon 192.168.1.10    # Check anonymous FTP login
```

---

## 9. Firewall Evasion & Spoofing
Bypass detection (lab use only).
```bash
nmap -f 192.168.1.10             # Fragment packets
nmap --source-port 53 192.168.1.10   # Use specific source port
nmap -D RND:10 192.168.1.10      # Decoy scan
nmap -S 192.168.1.200 192.168.1.10   # Spoof source IP
```

---

## 10. Common Practical Workflows

### 🔹 Full Scan of a Host
```bash
nmap -A -p- 192.168.1.10
```

### 🔹 Scan Entire Subnet
```bash
nmap -sS -T4 192.168.1.0/24
```

### 🔹 Vulnerability Check
```bash
nmap -sV --script=vuln 192.168.1.10
```

### 🔹 Web Server Enumeration
```bash
nmap -p 80,443 --script=http-enum 192.168.1.10
```

---

# ✅ Quick Summary
- **Discovery:** `-sn`, `-Pn`  
- **Ports:** `-p`, `-p-`, `-F`  
- **Services:** `-sV`  
- **OS:** `-O`, `-A`  
- **Scan Types:** `-sS`, `-sT`, `-sU`, `-sA`, `-sN`, `-sX`  
- **Timing:** `-T0` to `-T5`  
- **Output:** `-oN`, `-oX`, `-oG`  
- **Scripts:** `--script=vuln`, `--script=http-enum`  
- **Evasion:** `-f`, `-D`, `-S`, `--source-port`  

---

⚠️ **Note:** Use these commands only in **authorized labs or test environments**. Running scans against systems without permission is illegal.

---

