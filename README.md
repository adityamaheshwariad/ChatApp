Company: CODTECH IT SOLUTIONS

Intern Name: Aditya Maheshwari
Intern ID: :CT06DN848
Domain: Full Stack Web Development
Duration: 6 Weeks
Mentor: Neela Santosh
 ChatApp 🚀

Secure, multi‑threaded chat application with end‑to‑end encryption, built as part of my internship (Task 2 of 4).

 Tech Stack

- **Python** for server and client
- **Socket Programming** for real-time communication (multi‑threaded)
- **RSA Encryption** for message security (end-to-end)

 Project Overview

This application implements a secure chat environment:

- Multi‑threaded server handles multiple clients concurrently.
- Clients connect via sockets to the server.
- All messages are encrypted using RSA before transmission.
- Only intended recipients can decrypt messages, ensuring privacy.

 Features

- Supports multiple simultaneous clients (multi-threading).
- Secure communications using RSA public/private key pairs.
- Simple GUI (if implemented) or console-based interface.
- Graceful connection/disconnection handling.

 Repository Structure

ChatApp/
├── client.py # Chat client
├── server.py # Multi‑threaded chat server
├── crypto_utils.py # RSA key generation & encryption helper functions
├── requirements.txt # List of Python dependencies
└── README.md # This documentation file


 Setup & Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/adityamaheshwariad/ChatApp.git
   cd ChatApp
   
Create and activate a virtual environment:

python3 -m venv venv
source venv/bin/activate

Install dependencies:
pip install -r requirements.txt

Running the Application
 Generate RSA keys
bash
Copy
Edit

python crypto_utils.py generate_keys

python crypto_utils.py generate_keys
This creates private_key.pem and public_key.pem.

Start the Server
python server.py


Launch a Client
In a new terminal for each user:
python client.py


 Usage & Workflow
Each client generates an RSA key pair (via crypto_utils.py or built-in logic).

The server securely exchanges public keys with clients.

Messages are encrypted with the recipient’s public key and decrypted with their private key.

Clients can send/receive messages; the server routes encrypted payloads.

 RSA Encryption Workflow
Sender: Reads recipient’s public key → encrypts message → sends ciphertext to server.

Server: Receives ciphertext → forwards it without decrypting.

Recipient: Uses private key to decrypt message securely.

 Known Limitations & Future Improvements
Currently supports only one‑on‑one chat (no group chat).

No visual GUI – purely console-driven.

Missing features: authentication, typing indicators, message persistence.

Possible enhancements: group chats, GUI (e.g. with Tkinter), message history via database.

 Intern Task Context
This was developed as Task 2 of 4 during my internship. It aimed to demonstrate:

Real-time network programming with Python sockets.

Secure message encryption using RSA.

Thread-safe handling of multiple concurrent clients.

📋 License
Distributed under the MIT License. See LICENSE for details.

🙋‍♂️ Contact & Credits
Created by Aditya Maheshwari as part of CodTechItSolutions.
For questions or feedback, reach out via GitHub or email.







