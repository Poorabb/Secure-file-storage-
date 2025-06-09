# 🔐 Secure File System - Python Encryption Tool

A simple, interactive **text file encryption system** written in Python.  
It allows users to **securely create, encrypt, and view text files** using password-derived keys and the Fernet encryption module from the `cryptography` library.

---

## ✨ Features

- 🔑 Password-protected access
- 🔐 AES-based encryption using Fernet
- 📄 Create encrypted text files
- 👀 Decrypt and read only with correct credentials
- 📁 Automatically lists all `.txt` files in a secure folder

---

## 🧠 How It Works

1. User logs in using a **hardcoded password**.
2. If access is granted:
   - Option 1: Create a new file → Data is encrypted and saved
   - Option 2: View an existing file → Decrypted only with the correct password
3. Encryption is done using **Fernet symmetric encryption**.
4. The password is turned into a key using **PBKDF2 HMAC** with SHA-256 and a fixed salt.

---

## 🧰 Requirements

- Python 3.6 or above
- [`cryptography`](https://pypi.org/project/cryptography/)

### 📦 Installation and Usage

```bash
pip install cryptography

$ python secure_file_system.py

Enter password to login: One1two2
ACCESS GRANTED  ✅


			WELCOME TO THE SECURE FILE SYSTEM 📁

1. Create New file.
2. View existing files.
Enter command[1/2]: 1
Enter name for new file: secret_notes
Enter the file data: This is a very sensitive message.
File encrypted and saved successfully!

