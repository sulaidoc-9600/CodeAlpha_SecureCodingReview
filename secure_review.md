# Secure Coding Review — Sample Project
👤 Author: Sulaiman  
🏢 Internship: CodeAlpha — Cyber Security Internship  

---

## 🔍 Overview
This report analyses a small login code snippet to identify possible security flaws and recommend fixes.

---

## 🧩 Code Snippet (for review)
```python
# login.py (example)
username = input("Enter username: ")
password = input("Enter password: ")

if username == "admin" and password == "12345":
    print("Login successful!")
else:
    print("Invalid credentials")
```

---

## 🚨 Findings

1️⃣ **Hardcoded credentials**  
- Issue: Password “12345” is visible in the code.  
- Fix: Store passwords securely in a database with hashing (bcrypt / argon2).

2️⃣ **Plaintext password input**  
- Issue: Password typed directly, not masked.  
- Fix: Use a password input library or front-end masking.

3️⃣ **No input validation**  
- Issue: Username/password not validated for length or characters.  
- Fix: Add checks for empty fields, minimum length, etc.

4️⃣ **No encryption or hashing**  
- Issue: Password compared directly in code.  
- Fix: Hash stored passwords and compare hashes.

5️⃣ **No logging or access control**  
- Issue: Code gives same message for all users.  
- Fix: Implement user roles and logging for login attempts.

---

## 🛠️ Recommendations

✅ Use environment variables for credentials  
✅ Implement hashed password storage (bcrypt/argon2)  
✅ Add input validation for all user data  
✅ Use logging for authentication attempts  
✅ Avoid displaying sensitive information

---

## 📦 Conclusion
This review identifies basic vulnerabilities and provides fixes that align with secure coding practices.  
Following these steps ensures better protection against credential leaks and brute-force attacks.

---

📅 Date: 22 October 2025  
✅ Completed by Sulaiman for CodeAlpha Cyber Security Internship
