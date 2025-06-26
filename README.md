# Decryption-Tool
Custom File Encryption/Decryption Tool 🔐
This is a simple command-line Python tool for encrypting and decrypting files using AES in CBC mode with PBKDF2 for key derivation. It provides a secure way to protect your sensitive files with a password. ✨

Features
Symmetric Encryption: Uses AES (Advanced Encryption Standard) in CBC (Cipher Block Chaining) mode. 🔒

Key Derivation: Employs PBKDF2 with SHA256 and a random salt to securely derive a strong encryption key from your password. 🔑

Random Salt and IV: Generates a unique salt and Initialization Vector (IV) for each encryption, enhancing security. 🎲

File-based Operations: Encrypts an input file to an output file, and decrypts an encrypted file back to its original form. 📁➡️🔒 / 🔒➡️📁

Error Handling: Includes basic error handling for file not found, incorrect password, and other common issues. ⚠️

Technologies Used
Python 3.x 🐍

cryptography library: Python's leading cryptographic library for secure and efficient crypto operations. 💪

os, secrets, hashlib, base64 modules: For file system interactions, secure random number generation, hashing, and encoding. 💻

Getting Started
Follow these steps to set up and use the Encryption/Decryption Tool on your local machine. 🚀

Prerequisites
Python 3.7 or newer installed on your system. You can download it from python.org. ✅

Installation
Save the Code:
Save the provided Python code into a file named encryption_tool.py (or any .py name you prefer) in a directory on your computer. 💾

Example:

my_crypto_tools/
└── encryption_tool.py

Open your Terminal or Command Prompt:
Navigate to the directory where you saved encryption_tool.py. 🖥️

cd path/to/my_crypto_tools

Create a Virtual Environment (Recommended):
It's good practice to create a virtual environment to manage project dependencies and avoid conflicts with your system's Python packages. 🌍

python -m venv venv

Activate the Virtual Environment:

On Windows:

.\venv\Scripts\activate

On macOS/Linux:

source venv/bin/activate

You should see (venv) at the beginning of your terminal prompt, indicating the virtual environment is active. 👍

Install Dependencies:
This tool relies on the cryptography library. 📦

pip install cryptography

How to Use
Ensure your virtual environment is active before running the script. 🏃‍♀️

Navigate to your project directory in your terminal/command prompt. 📂

Run the script:

python encryption_tool.py

Follow the on-screen prompts: 💬

--- Custom File Encryption/Decryption Tool ---
Choose an action:
1. Encrypt File
2. Decrypt File
Enter your choice (1 or 2):

Encrypting a File 📈
Choose option 1 for Encryption.

Enter your choice (1 or 2): 1

Provide the paths:

Input file: The full path to the file you want to encrypt. ➡️📄

Example: my_document.txt (if in the same directory) or C:\Users\YourUser\Documents\secret_report.pdf

Output file: The desired name and path for the encrypted file. It's common to add an .aes or .enc extension. 💾🔒

Example: my_document.aes or C:\Users\YourUser\Documents\secret_report.pdf.enc

Enter your password:

Crucial: Remember this password! You will need the exact same password to decrypt the file. Choose a strong, unique password. ⚠️🔑

Example interaction:

Enter the path to the file to encrypt: my_secret_data.txt
Enter the desired output path for the encrypted file (e.g., myfile.aes): my_secret_data.txt.enc
Enter your encryption password: mySuperSecretPassword123!
File encrypted successfully: my_secret_data.txt.enc ✨

Decrypting a File 📉
Choose option 2 for Decryption.

Enter your choice (1 or 2): 2

Provide the paths:

Input encrypted file: The full path to the encrypted file (e.g., my_secret_data.txt.enc). ⬅️🔒

Output file: The desired name and path for the decrypted file. Make sure it has the original file's extension if you want to open it correctly (e.g., my_recovered_data.txt). 💾📄

Enter your password:

You must enter the exact same password that was used to encrypt the file. If the password is incorrect or the file is corrupted, decryption will fail with a Padding verification failed error. ❌🔑

Example interaction:

Enter the path to the file to decrypt (e.g., myfile.aes): my_secret_data.txt.enc
Enter the desired output path for the decrypted file: my_recovered_data.txt
Enter your decryption password: mySuperSecretPassword123!
File decrypted successfully: my_recovered_data.txt ✅

Important Notes
Password Security: The security of your encrypted file directly depends on the strength of your password. Use long, complex passwords that are unique to this tool. 🛡️

Lost Password: If you lose your password, the encrypted file cannot be recovered. There is no backdoor. 🚫

File Integrity: Ensure the input file for decryption is not corrupted. Any corruption can lead to decryption failures. 💔

Overwriting Files: Be careful when specifying output file paths to avoid accidentally overwriting existing files. 🔄

Performance: For very large files, the encryption/decryption process might take some time, as it reads and writes in chunks. ⏳
