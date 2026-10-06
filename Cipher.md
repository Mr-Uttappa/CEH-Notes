A **cipher** is the algorithm or method used to perform encryption and decryption. In cryptography, the cipher defines *how* plaintext is transformed into ciphertext and back again using keys. Think of it as the “recipe” for scrambling and unscrambling information.

---

## 📌 Cipher Types

### 1. **Classical Ciphers**
- **Substitution Cipher**  
  - Each letter or symbol is replaced with another.  
  - Example: Caesar Cipher (shift letters by 3).  
- **Transposition Cipher**  
  - Rearranges the order of characters without changing them.  
  - Example: Rail Fence Cipher.  
- **Polyalphabetic Cipher**  
  - Uses multiple substitution alphabets.  
  - Example: Vigenère Cipher.  

---

### 2. **Modern Symmetric Ciphers**
- **Block Ciphers**  
  - Encrypt fixed‑size blocks of data (e.g., 128 bits).  
  - Example: AES, DES, Blowfish.  
- **Stream Ciphers**  
  - Encrypt data one bit/byte at a time, often using a keystream.  
  - Example: RC4.  

---

### 3. **Asymmetric Ciphers**
- Use **public key** for encryption and **private key** for decryption.  
- Examples: RSA, ECC (Elliptic Curve Cryptography).  
- Often used for secure key exchange and digital signatures.  

---

### 4. **Hash Functions (One‑Way Ciphers)**
- Not reversible — used to verify integrity.  
- Examples: SHA‑256, MD5.  
- Common in password storage and digital signatures.  

---

## ⚡ Cipher Modes (for Block Ciphers)
Block ciphers often use **modes of operation** to handle larger data:
- **ECB (Electronic Codebook)** → Simple, but insecure (patterns leak).  
- **CBC (Cipher Block Chaining)** → Each block depends on the previous one.  
- **CFB/OFB** → Turn block ciphers into stream ciphers.  
- **CTR (Counter Mode)** → Uses counters for parallel encryption.  

---

## 🛡️ Why Ciphers Matter
- They define the **strength of encryption**.  
- Weak ciphers (like DES, RC4) are deprecated.  
- Strong ciphers (AES, RSA, ECC) are standard in modern security (HTTPS, VPNs, banking).  

---

✅ **Summary:** A cipher is the algorithm that scrambles and unscrambles data. Types include **classical (substitution, transposition)**, **modern symmetric (block, stream)**, **asymmetric (RSA, ECC)**, and **hash functions**. Cipher modes (CBC, CTR, etc.) define how block ciphers process large data securely.  

Would you like me to create a **comparison table of cipher types with examples, strengths, and weaknesses** so you can use it as a CEH study reference?




