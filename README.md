# 📚 Study Sathi

**Study Sathi** is a collaborative group-study web platform that lets students create and join subject-based study groups, share notes, and learn together. Built with Flask and designed for simplicity, speed, and ease of deployment.

🔗 **Live Demo:** https://studysathi-production.up.railway.app

---

## ✨ Features

- 🔐 **User Authentication** — Secure signup/login with hashed passwords (Werkzeug security)
- 👥 **Study Groups** — Create subject-specific groups with descriptions
- 🤝 **Join & Collaborate** — Browse and join groups created by other students
- 📄 **Note Sharing** — Upload and share study notes within a group
- 📊 **Dashboard** — View your groups and discover new ones with live member counts
- 💬 **Flash Messaging** — Clear user feedback for every action (success/error/info)

---

## 🛠️ Tech Stack

| Layer          | Technology                        |
|----------------|------------------------------------|
| Backend        | Python, Flask                      |
| Database       | SQLite                             |
| Auth           | Werkzeug (password hashing)        |
| Frontend       | HTML, Jinja2 Templates             |
| File Handling  | Flask file uploads                 |
| Deployment     | Railway (Docker-ready)             |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- pip

### Installation

```bash
# Clone the repository
git clone https://github.com/Prashant12588/study-sathi.git
cd study-sathi

# Install dependencies
pip install -r requirements.txt

# Create the uploads folder (required for note uploads)
mkdir uploads

# Run the app
python app.py
```

The app will be available at `http://localhost:5000`

---

## 📁 Project Structure

```
study-sathi/
├── app.py              # Main Flask application
├── study_sathi.db      # SQLite database (auto-created on first run)
├── uploads/            # Uploaded notes storage
├── templates/          # HTML templates (Jinja2)
│   ├── index.html
│   ├── signup.html
│   ├── login.html
│   ├── dashboard.html
│   ├── create_group.html
│   └── group.html
└── README.md
```

---

## 🗄️ Database Schema

- **users** — id, name, email, password (hashed), created_at
- **groups** — id, name, subject, description, owner_id, created_at
- **memberships** — user_id, group_id (many-to-many join table)
- **notes** — id, group_id, user_id, filename, original_name, uploaded_at

---

## 🔮 Roadmap / Future Improvements

- [ ] Migrate to PostgreSQL for persistent, production-grade storage
- [ ] Add real-time group chat
- [ ] File preview support for uploaded notes
- [ ] Group admin controls (remove members, edit group details)
- [ ] Email verification on signup

---

## 👤 Author

**Prashant Yadav**
B.Tech CSE (Cloud Computing & DevOps) — Uttaranchal University

- GitHub: [@Prashant12588](https://github.com/Prashant12588)
- LinkedIn: [Prashant Yadav](https://linkedin.com/in/prashant-yadav-343852204)
- Email: yadavprashant7979@gmail.com

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
