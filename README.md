# GitLab to GitHub Mirror Repository

This project demonstrates how to automatically mirror a GitLab repository to GitHub using **GitLab Repository Mirroring (Push)**.

Whenever code is pushed to GitLab, it is automatically synced to GitHub.

---

## 🛠 Prerequisites

Before starting, make sure you have:

- A GitLab account
- A GitHub account
- Git installed on your system
- Basic knowledge of Git commands
- GitHub Personal Access Token (Classic)

---

## 📁 Project Structure

gitlab-mirror-repo/
├── README.md
├── home.html
└── about.html

---

## 🚀 Step 1: Create Repositories

### 1️⃣ Create a GitLab Repository
- Repository name: `gitlab-mirror-repo`
- Visibility: Public (or Private)

### 2️⃣ Create a GitHub Repository
- Repository name: `github-mirror-repo`
- Visibility: Public (or Private)

---

## 🔐 Step 2: Generate GitHub Personal Access Token

1. Go to **GitHub → Settings → Developer settings**
2. Click **Personal access tokens → Tokens (classic)**
3. Generate a new token with:
   - ✅ `repo` permission
4. Copy the token (you won’t see it again)

---

## 🔁 Step 3: Configure GitLab Repository Mirroring

1. Open your **GitLab project**
2. Go to  
   **Settings → Repository → Mirroring repositories**
3. Click **Add new**
4. Fill details:
   - **Git repository URL**:
     ```
     https://<GITHUB_USERNAME>:<GITHUB_TOKEN>@github.com/<username>/github-mirror-repo.git
     ```
   - **Direction**: Push
   - **Authentication**: Username + Token
5. Click **Mirror repository**

✅ Status should show **Last successful update**

---

## 💻 Step 4: Clone GitLab Repository Locally

```bash
git clone https://gitlab.com/tk4924232/gitlab-mirror-repo.git
cd gitlab-mirror-repo

---

## 💻 Step 5: Add Files and Push to GitLab

<h1>This file is from GitLab</h1>

```bash
git add .
git commit -m "gitlab added"
git push origin main

---

## Step 6: Work with Branches 

Create and switch to dev branch

```bash
git checkout -b dev

Add about.html

git add .
git commit -m "added about"
git push -u origin dev

---

## step 7: Create Repository in GitHub

Created new repo: github-mirror-repo

Did not initialize with README

Generate GitHub Personal Access Token

GitHub → Settings → Developer Settings

Personal Access Token (Classic)

Enable repo permission

## step 8:Configure Push Mirroring in GitLab

Go to:

GitLab → Settings → Repository → Mirroring repositories

Add GitHub URL:

https://<username>:<token>@github.com/<username>/github-mirror-repo.git

Select:

Direction: Push

Save.

Result

All files synced from GitLab to GitHub

Branches and commits mirrored automatically

Changes update automatically after push

Project Structure
gitlab-mirror-repo/
│
├── README.md
├── home.html
└── about.html
Author

Tejasvi Kadam
