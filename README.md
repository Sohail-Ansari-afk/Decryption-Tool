# 🔐 Custom File Encryption/Decryption Tool

Secure your sensitive files with this simple yet powerful **command-line encryption/decryption tool** built in Python. This script uses **AES encryption** with **PBKDF2 key derivation**, ensuring robust protection through password-based access.

---

## ✨ Features

- 🔒 **Symmetric Encryption**: Uses AES (Advanced Encryption Standard) in CBC (Cipher Block Chaining) mode.
- 🔑 **Key Derivation**: Utilizes PBKDF2 with SHA256 and random salt for strong password-based key generation.
- 🎲 **Random Salt & IV**: Each encryption generates a new salt and IV for enhanced security.
- 📁 **File-based Operations**: Encrypt or decrypt entire files quickly and securely.
- ⚠️ **Error Handling**: Detects incorrect passwords, missing files, and more with clear error messages.

---

## 🧰 Technologies Used

- 🐍 Python 3.x
- 📦 [`cryptography`](https://pypi.org/project/cryptography/) - Python’s premier cryptographic library
- 🔧 Built-in modules: `os`, `secrets`, `hashlib`, `base64`

---

## 🚀 Getting Started

### ✅ Prerequisites

- Python 3.7 or higher  
  [Download Python](https://www.python.org/downloads/)

---

## 🛠️ Installation

### 1. 📥 Save the Script

Save the provided Python code into a file named `encryption_tool.py` (or any `.py` file you prefer):

```

my\_crypto\_tools/
└── encryption\_tool.py

````

### 2. 💻 Open Terminal

Navigate to your project folder:
```bash
cd path/to/my_crypto_tools
````

### 3. 🌍 Create Virtual Environment (Recommended)

```bash
python -m venv venv
```

Activate it:

* **Windows**

  ```bash
  .\venv\Scripts\activate
  ```

* **macOS/Linux**

  ```bash
  source venv/bin/activate
  ```

### 4. 📦 Install Dependencies

```bash
pip install cryptography
```

---

## 🧪 How to Use

Make sure your virtual environment is active.

### 🔐 Encrypt a File

1. Run the script:

   ```bash
   python encryption_tool.py
   ```

2. Choose Encryption:

   ```
   --- Custom File Encryption/Decryption Tool ---
   Choose an action:
   1. Encrypt File
   2. Decrypt File
   Enter your choice (1 or 2): 1
   ```

3. Provide:

   * 📄 Input file path (e.g., `secret.txt`)
   * 💾 Output file path (e.g., `secret.aes`)
   * 🔑 Strong password (e.g., `MySecurePassword123!`)

4. ✅ Success message:

   ```
   File encrypted successfully: secret.aes
   ```

---

### 🔓 Decrypt a File

1. Run the script:

   ```bash
   python encryption_tool.py
   ```

2. Choose Decryption:

   ```
   Enter your choice (1 or 2): 2
   ```

3. Provide:

   * 🔒 Encrypted file path (e.g., `secret.aes`)
   * 💾 Output file path (e.g., `restored.txt`)
   * 🔑 Password used during encryption

4. ✅ Success message:

   ```
   File decrypted successfully: restored.txt
   ```

---

## ⚠️ Important Notes

* 🛡️ **Password Strength**: Use long, complex, and unique passwords.
* 🚫 **No Password Recovery**: There is no way to recover the file without the correct password.
* 💔 **Corruption Risks**: Corrupted files or incorrect decryption attempts may cause failure.
* 🔄 **Overwriting**: Double-check output paths to avoid overwriting important files.
* ⏳ **Large Files**: The process may take longer for large files.

---

## 📄 License

This project is open-source and free to use. Licensed under the MIT License.

---

## 👤 Author

Built with ❤️ by Sohail-Ansari

