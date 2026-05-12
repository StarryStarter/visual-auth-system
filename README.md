# Visual Auth System — Graphical Password Authentication

A password-free authentication system where users log in by arranging images in the correct order instead of typing a password. Built with Python and Flask.

---

## How It Works

Traditional passwords are vulnerable to keyloggers and shoulder-surfing. This system replaces them with a **drag-and-drop image sequence** that only the user knows.

**Registration:**
1. Upload 9 personal images
2. Arrange them in a specific order to create your graphical password

**Login:**
1. Enter your registered email
2. The 9 images are shown in a randomized order
3. Drag and drop them back into your secret sequence to authenticate

If the arrangement is wrong, the images are reshuffled. After **4 failed attempts**, the account is automatically blocked.

---

## Features

- Image-based authentication (no text passwords)
- Randomized image display on every login attempt to prevent pattern observation
- Account lockout after 4 consecutive failures
- Session protection: dashboard inaccessible without authentication
- SQLite database for storing users, images, and sequence hashes

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python, Flask |
| Database | SQLite via SQLAlchemy |
| Frontend | HTML, CSS, JavaScript |

---

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/StarryStarter/visual-auth-system.git
cd visual-auth-system
```

### 2. Install dependencies
```bash
pip install flask flask_sqlalchemy
```

### 3. Run the app
```bash
python app.py
```

Then open [http://localhost:5000](http://localhost:5000) in your browser.

---

## Security Considerations

- Image sequences are stored as hashed values, not raw order data
- Brute-force attempts are limited by account lockout
- All routes check session validity before serving protected pages

---

## Topics
`python` `flask` `authentication` `graphical-password` `security` `sqlite` `sqlalchemy` `web-security`
