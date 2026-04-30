# Study Sathi — Group Study Web App

A Flask web application for group study collaboration, deployed on AWS.

## Tech Stack
- **Backend**: Python Flask
- **Database**: SQLite (local) → AWS RDS (production)
- **Storage**: Local uploads → AWS S3 + CloudFront
- **Hosting**: AWS EC2

## Run Locally
```bash
pip install flask werkzeug
python app.py
```
Open http://localhost:5000

## Project Structure
```
study_sathi/
├── app.py              # Flask app + all routes
├── requirements.txt
├── templates/
│   ├── base.html       # Shared layout + navbar
│   ├── index.html      # Landing page
│   ├── login.html      # Login page
│   ├── signup.html     # Signup page
│   ├── dashboard.html  # User dashboard
│   ├── create_group.html
│   └── group.html      # Group detail + upload
└── uploads/            # Local file storage (→ S3 later)
```

## Features
- User signup / login / logout
- Create and join study groups
- Upload study notes (PDF, images, docs)
- View group members and uploaded files

## Next Steps (AWS Integration)
- Phase 2: Replace local uploads with S3 + CloudFront
- Phase 3: Lambda for image resize / email notifications
- Phase 4: Cognito for auth, SES for emails
- Phase 5: CloudWatch monitoring, CodePipeline CI/CD
