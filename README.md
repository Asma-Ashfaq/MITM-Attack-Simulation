# 🔐 MITM Attack Simulation in C++

## 📌 Project Overview
This project demonstrates a **Man-in-the-Middle (MITM) attack** using C++ and TCP socket programming. It simulates communication between a client and a server where an attacker intercepts and modifies messages. The project also implements a basic encryption mechanism to demonstrate how secure communication can prevent such attacks.

---

## 🎯 Objectives
- Simulate a MITM attack in a controlled environment  
- Demonstrate message interception and modification  
- Implement basic encryption for prevention  
- Understand network security vulnerabilities  

---

## 🧠 What is MITM Attack?
A Man-in-the-Middle (MITM) attack occurs when an attacker secretly intercepts communication between two parties and can read or alter the transmitted data.


Client → Attacker → Server


---

## ⚙️ Technologies Used
- C++  
- TCP Socket Programming  
- Winsock (Windows API)  
- Visual Studio / VS Code  

---

## 📁 Project Structure

MITM-Project/
│── client.cpp
│── server.cpp
│── attacker.cpp
│── README.md


---

## 🚀 How It Works

### 🔴 Without Encryption
1. Client sends message  
2. Attacker intercepts message  
3. Attacker modifies message  
4. Server receives modified message  

Example:

Hello → Hello [HACKED]


---

### 🔐 With Encryption
1. Client encrypts message  
2. Attacker intercepts encrypted data  
3. Server decrypts message  

Example:

Hello → Xy@#!! → Hello


---

## ▶️ How to Run

### 🔧 Compile
```bash
g++ client.cpp -o client.exe -lws2_32
g++ server.cpp -o server.exe -lws2_32
g++ attacker.cpp -o attacker.exe -lws2_32
▶️ Execution Order (Important)

Run in three separate terminals:

.\server.exe
.\attacker.exe
.\client.exe
📸 Expected Output
🟢 Client
Enter message: Hello
Reply: OK
🟡 Attacker
Intercepted (Encrypted): Xy@#!!
🔵 Server
Received (Decrypted): Hello
🔐 Prevention Techniques
Encryption (XOR used in this project)
SSL/TLS protocols
Digital certificates
Authentication mechanisms
⚠️ Limitations
Runs only on localhost
Uses simple encryption (not secure for real-world use)
No graphical interface
📌 Conclusion

This project successfully demonstrates how a MITM attack works and how encryption helps protect communication by ensuring data confidentiality and integrity.

👩‍💻 Author

Asma Ashfaq
Undergraduate Student – Information Technology

⭐ Note

This project is for educational purposes only to understand security concepts, attacks, and defense mechanisms.
