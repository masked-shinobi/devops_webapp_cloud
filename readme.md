🚀 DevOps WebApp Cloud — CI/CD Automation

📌 Project Overview

This project demonstrates an end-to-end DevOps automation pipeline using:

- Git & GitHub for version control
- GitHub Actions for Continuous Integration (CI)
- Slack for ChatOps notifications
- Netlify for Continuous Deployment (CD)
- Static website hosting

Whenever code is pushed:

✅ CI pipeline runs automatically
✅ Slack receives build notification
✅ Website auto-deploys

---

🌍 Live Website

Paste your deployed site URL here.

---

🧰 Technologies Used

- HTML
- Git & GitHub
- GitHub Actions
- Slack Incoming Webhooks
- Netlify

---

📁 Project Structure

devops-webapp-cloud/
│
├── index.html
└── .github/
    └── workflows/
        └── ci.yml

---

🧩 Setup Instructions

1️⃣ Clone Repository

git clone <your-repo-url>
cd devops-webapp-cloud

2️⃣ Initialize & Push (if starting fresh)

git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main

---

🧩 CI Pipeline Configuration

Create:

.github/workflows/ci.yml

Paste:

name: DevOps CI Pipeline

on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3

    - name: Build Step
      run: echo "Build successful!"

    - name: Slack Notification
      run: |
        curl -X POST -H 'Content-type: application/json' \
        --data '{"text":"✅ Build Successful!"}' \
        ${{ secrets.SLACK_WEBHOOK }}

---

🧩 Add Slack Secret

Repository → Settings → Secrets and variables → Actions

Add:

Name: SLACK_WEBHOOK
Value: (paste webhook URL)

---

🧩 Deployment

Import the repository into Netlify and enable auto-deploy.

---

🧩 Test Automation

After making changes:

git add .
git commit -m "update"
git push

Expected Results

✔ CI pipeline runs
✔ Slack notification received
✔ Website updates automatically

---

📸 Required Outputs

- GitHub Actions workflow run screenshot
- Slack notification screenshot
- Live deployed URL
- Build logs

---

🎯 DevOps Concepts Demonstrated

✔ Continuous Integration
✔ Continuous Deployment
✔ ChatOps Notifications
✔ Version Control Workflow
✔ Cloud Deployment

---

👨‍💻 Author

SANJAY BASKAR

---