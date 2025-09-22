# nodejs-demo-app

Simple Express app for CI/CD demo. Tests use Jest + Supertest. Dockerfile included

📌 Project Overview

This project is a simple Node.js application created as part of my DevOps internship. The main goal was to set up a CI/CD pipeline using GitHub Actions that automatically runs tests and ensures code quality before deployment.

⚙️ Tech Stack

Node.js (Application)

npm (Package Manager)

Jest (Testing Framework)

Docker for deployment
GitHub Actions (CI/CD Pipeline)

🚀 CI/CD Pipeline Workflow

The pipeline was designed with the following stages:

Checkout Code – Clone repository from GitHub.

Setup Node.js – Configure Node.js environment.

Install Dependencies – Run npm install.

Run Tests – Execute npm test with Jest.

(Optional) Deployment stage (planned, not fully implemented).

❌ Current Issue

During pipeline execution, the build fails at the install/test step due to an npm error:

JSONError: Unexpected token ﻿ in JSON at position 0 in package.json


This happens because of a hidden character in the package.json file (likely caused by editing files in Notepad).

🔍 Debugging Attempts

Verified package.json formatting.

Reinstalled node modules locally.

Tried running npm install on local machine (works fine).

Identified potential BOM (Byte Order Mark) issue in package.json.

📚 Learnings

Importance of using proper editors (VS Code instead of Notepad) for JSON/YAML files.

Gained hands-on experience in writing GitHub Actions workflows.

Understood how pipeline logs help in debugging.

Learned about common npm and Node.js CI/CD issues.

✅ Next Steps

If I had more time, I would:

Recreate package.json without BOM issue.

Add a deployment stage to a cloud provider (AWS/Heroku).

Implement caching in pipeline for faster builds.

📖 How to Run Locally

Clone the repo:

git clone <repo-url>
cd nodejs-demo-app

Install dependencies: npm install

Run tests: npm test

Although the pipeline is failing due to a minor npm configuration issue, this project demonstrates my understanding of DevOps practices, CI/CD setup, and debugging workflows.

If possible, please guide me for betterment to any mode of communication. Some screenshots below i took when docker run and container works on localhost<img width="1918" height="1079" alt="Screenshot 2025-09-22 193701" src="https://github.com/user-attachments/assets/f09543c8-60d0-4567-9d17-a56e182b1621" />
<img width="1919" height="957" alt="Screenshot 2025-09-22 190909" src="https://github.com/user-attachments/assets/4fd3fd79-596c-43d5-aa9e-3df27cd4086b" />
<img width="1717" height="926" alt="Screenshot 2025-09-22 190831" src="https://github.com/user-attachments/assets/ca9f8d1a-c98a-452e-a707-160821dbb51b" />
<img width="1714" height="919" alt="Screenshot 2025-09-22 190433" src="https://github.com/user-attachments/assets/60ac7100-af65-42d7-a59a-7719671f8323" />

