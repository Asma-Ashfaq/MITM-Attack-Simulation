MITM Attack Simulation in C++
📌 Project Overview

This project demonstrates a Man-in-the-Middle (MITM) attack using C++ and TCP socket programming. It simulates communication between a client and a server where an attacker intercepts and modifies messages. The project also implements a basic encryption mechanism to demonstrate how secure communication can prevent such attacks.

🎯 Objectives
Simulate a MITM attack in a controlled environment
Show how an attacker can intercept and modify messages
Demonstrate prevention using encryption
Understand network security vulnerabilities
🧠 What is MITM Attack?

A Man-in-the-Middle attack occurs when an attacker secretly intercepts communication between two parties and can read or alter the transmitted data.

Client → Attacker → Server
⚙️ Technologies Used
C++
TCP Socket Programming
Winsock (Windows API)
VS Code / Visual Studio
📁 Project Structure
MITM-Project/
│── client.cpp
│── server.cpp
│── attacker.cpp
│── README.md
🚀 How It Works
🔴 Without Encryption
Client sends message
Attacker intercepts message
Attacker modifies message
Server receives modified message

Example:

Hello → Hello [HACKED]
🔐 With Encryption
Client encrypts message
Attacker intercepts (cannot understand)
Server decrypts message

Example:

Hello → Xy@#!! → Hello
▶️ How to Run
🔧 Compile
g++ client.cpp -o client.exe -lws2_32
g++ server.cpp -o server.exe -lws2_32
g++ attacker.cpp -o attacker.exe -lws2_32
▶️ Execution Order (Important)

Run in 3 separate terminals:

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
Uses basic encryption (not secure for real-world use)
No graphical interface
📌 Conclusion

This project successfully demonstrates how MITM attacks work and how encryption can protect communication by ensuring confidentiality and integrity.

👩‍💻 Author

Asma Ashfaq
Information Technology Student

⭐ Note

This project is for educational purposes only to understand security vulnerabilities and defense mechanisms.
