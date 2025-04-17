# 🔐 Secure Multi-User Data Encryption System

A Streamlit-based web application that allows multiple users to **register**, **login**, and **securely store/retrieve encrypted data** using their own encryption keys.

---

## 🚀 Features

- 🧾 **User Registration**  
- 🔐 **Secure Login with Lockout Mechanism**  
- 🔒 **PBKDF2 & Fernet Encryption**  
- 🧠 **Per-user Data Isolation**  
- 🔑 **Passphrase-Based Encryption & Decryption**  
- ⏱️ **Lockout After 3 Failed Login Attempts (60s)**  
- 📂 **Store Multiple Entries Per User**  
- 🧹 **Simple & Clean Streamlit Interface**  

---

## 📁 File Structure

```
.
├── secure_data.json        # Stores all user data securely
├── app.py                  # Main Streamlit application file
├── README.md               # Project documentation
```

---

## 🔧 Requirements

- Python 3.7+
- Streamlit
- cryptography

### Install dependencies:

```bash
pip install streamlit cryptography
```

---

## ▶️ How to Run

```bash
streamlit run app.py
```

---

## 🧑‍💻 How It Works

### 🔐 Registration

Each user registers with:
- A **username**
- A **password** (hashed with PBKDF2)

### 🔑 Login

- Validates user credentials
- If 3 incorrect attempts: lockout for 60 seconds

### 🗃️ Store Data

- User inputs plain text + custom **passphrase**
- Data encrypted using **Fernet** with a derived key
- Stored in `secure_data.json`

### 🔍 Retrieve Data

- Users can see their encrypted entries
- Paste an encrypted string + the original passphrase to decrypt it

---

## 🔒 Security Details

- **Passwords** hashed with: `PBKDF2-HMAC-SHA256`
- **Encryption Key**: derived from user passphrase via PBKDF2
- **Encryption Algorithm**: `Fernet` from `cryptography` package
- Data is stored encrypted in a local JSON file

---

## 📸 Screenshots

> You can add Streamlit UI screenshots here for GitHub preview

---

## 💡 Future Improvements

- Add user deletion & password update feature  
- Move from local JSON to cloud DB  
- Deploy online with user sessions  
- Add file upload encryption support

---

## 👩‍💻 Author

**Izma Ikhlaque**  
[GitHub](https://github.com/IzmaRao) | [LinkedIn](https://www.linkedin.com/in/izma-21i/)  

---

## 📜 License

This project is licensed under the MIT License.
