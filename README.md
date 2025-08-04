# ALXprodev-advanced_git

# 📌 Git Flows Project

Welcome to the **Git Flows** project! This repository serves as a hands-on guide and demonstration of effective **Git workflows** used in collaborative software development, especially in teams. It showcases best practices using the Git version control system and adheres to a structured branching model to streamline development and deployment processes.

---

## 📖 Table of Contents

- [📌 Git Flows Project](#-git-flows-project)
- [📖 Table of Contents](#-table-of-contents)
- [📂 Project Structure](#-project-structure)
- [🚀 Project Goals](#-project-goals)
- [🧠 Key Concepts](#-key-concepts)
- [🌱 Git Flow Branching Strategy](#-git-flow-branching-strategy)
- [⚙️ Prerequisites](#️-prerequisites)
- [🛠️ Setup and Installation](#️-setup-and-installation)
- [📸 Example Git Flow Usage](#-example-git-flow-usage)
- [📦 Features](#-features)
- [📑 Git Best Practices](#-git-best-practices)
  
---

## 📂 Project Structure

```bash
git-flows-project/
├── README.md
├── .gitignore
├── docs/
│   └── workflow-diagram.png
├── src/
│   ├── index.js
│   └── features/
│       └── sampleFeature.js
└── .git/
```
## 🚀 Project Goals

- Demonstrate the use of Git Flow branching strategy.
- Simulate a real-world software development team environment.
- Showcase feature development, bug fixing, and release management using branches.
- Enforce Git best practices like clear commit messages, pull requests, and reviews.

---

## 🧠 Key Concepts

- **Version Control**: Tracking and managing changes to code.
- **Branching**: Creating parallel versions of the codebase for development.
- **Merging**: Integrating changes from different branches.
- **Tagging**: Marking versions/releases for reference.
- **Collaboration**: Working together with teammates on a shared codebase.

---

## 🌱 Git Flow Branching Strategy

This project uses the **Git Flow** model with the following branch types:

- **main/**: The production-ready branch. Only contains fully tested code.
- **develop/**: The integration branch for features before they are merged to `main`.
- **feature/**: Branches for new features (e.g., `feature/login-system`).
- **hotfix/**: Branches for urgent bug fixes (e.g., `hotfix/fix-crash`).
- **release/**: Branches for preparing a new production release (e.g., `release/v1.0.0`).
- **bugfix/**: Minor fixes or improvements that don't require a hotfix.

---

## ⚙️ Prerequisites

Make sure you have the following installed:

- **Git**
- **Terminal / Git Bash**
- **GitHub account** (optional for remote collaboration)

---

## 🛠️ Setup and Installation

```bash
# Clone the repository
git clone https://github.com/your-username/git-flows-project.git

# Navigate into the project
cd git-flows-project
```
## 📸 Example Git Flow Usage
### 🔧 Creating a Feature Branch
```bash
# Switch to develop
git checkout develop

# Create a feature branch
git checkout -b feature/add-authentication

# After making changes
git add .
git commit -m "feat: add user authentication system"
git push origin feature/add-authentication
```
### 🔁 Merging Feature into Develop
```
git checkout develop
git merge feature/add-authentication
git branch -d feature/add-authentication
```
### 🚀 Creating a Release
```
git checkout develop
git checkout -b release/v1.0.0

# Final changes (e.g., updating changelog)
git add .
git commit -m "chore: prepare v1.0.0 release"

git checkout main
git merge release/v1.0.0
git tag v1.0.0

git checkout develop
git merge release/v1.0.0
git branch -d release/v1.0.0
```
### 🐞 Creating a Hotfix
```
git checkout main
git checkout -b hotfix/fix-login-crash

# Fix the bug
git add .
git commit -m "fix: resolve crash on login for v1.0.0"

# Merge to main and tag
git checkout main
git merge hotfix/fix-login-crash
git tag v1.0.1

# Merge to develop
git checkout develop
git merge hotfix/fix-login-crash
git branch -d hotfix/fix-login-crash
```
## 📦 Features
- Demonstrates a full Git Flow branching model.

- Includes example scripts and logs.

- Documented Git workflow using markdown.

- Helpful for both solo developers and teams.

## 📑 Git Best Practices
- Use meaningful and consistent commit messages.

- Pull the latest changes before starting new work.

- Avoid working directly on main or develop.

- Frequently push your feature branch.

- Use Pull Requests for code reviews and collaboration.

- Keep branches focused and concise.

- Rebase with care; prefer merge for team projects.


## how to fork a repo.

### Create your branch:

```
git checkout -b feature/something
```
### Commit your changes:

```
git commit -m "feat: add something"
```
### Push to your branch:

```
git push origin feature/something
```
- Open a Pull Request.


### Initialize Git if not already done
```
git init
```
### Create the main and develop branches
```
git checkout -b main
git checkout -b develop
```
