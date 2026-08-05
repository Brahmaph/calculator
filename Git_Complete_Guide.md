# Git Complete Beginner to Professional Guide

## 1. Create a GitHub Repository

-   Sign in to GitHub.
-   Click **New Repository**.
-   Give it a name (e.g. `Calculator`).
-   Click **Create Repository**.

## 2. Create Your Project

``` text
Calculator/
├── index.html
├── style.css
├── script.js
└── README.md
```

## 3. Install Git

Download from https://git-scm.com

## 4. Configure Git (One Time)

``` bash
git --version
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

## 5. Open Git Bash

Right-click project folder → **Open Git Bash Here**

## 6. Initialize Git

``` bash
git init
```

## 7. Check Status

``` bash
git status
```

## 8. Stage Files

``` bash
git add .
# or
git add index.html
```

## 9. Commit

``` bash
git commit -m "Initial project setup"
```

## 10. View History

``` bash
git log
git log --oneline
```

## 11. Rename Default Branch

``` bash
git branch -M main
```

## 12. Connect to GitHub

``` bash
git remote add origin https://github.com/<username>/Calculator.git
git remote -v
```

## 13. Push to GitHub

``` bash
git push -u origin main
```

Future pushes:

``` bash
git push
```

------------------------------------------------------------------------

# Branching

## View Branches

``` bash
git branch
```

## Create a Branch

``` bash
git branch feature-login
```

## Create and Switch

``` bash
git switch -c feature-login
# or
git checkout -b feature-login
```

## Switch Branches

``` bash
git switch main
git switch feature-login
```

## Check Current Branch

``` bash
git branch
```

------------------------------------------------------------------------

# Working in a Branch

Modify files.

Check:

``` bash
git status
```

Stage:

``` bash
git add .
```

Commit:

``` bash
git commit -m "Added login page"
```

Push branch:

``` bash
git push -u origin feature-login
```

------------------------------------------------------------------------

# Merge Branch

Switch to main:

``` bash
git switch main
```

Merge:

``` bash
git merge feature-login
```

Push:

``` bash
git push
```

Delete local branch:

``` bash
git branch -d feature-login
```

Delete remote branch:

``` bash
git push origin --delete feature-login
```

------------------------------------------------------------------------

# Pull Latest Changes

``` bash
git pull
```

# Fetch Only

``` bash
git fetch
```

------------------------------------------------------------------------

# View Graph

``` bash
git log --oneline --graph --all
```

------------------------------------------------------------------------

# Daily Workflow

``` text
git pull
git switch -c feature-name
# Make changes
git status
git add .
git commit -m "Meaningful message"
git push -u origin feature-name
# Create Pull Request
git switch main
git pull
git merge feature-name
git push
```

------------------------------------------------------------------------

# Common Commands

  Command                    Purpose
  -------------------------- --------------------------
  git init                   Initialize repository
  git status                 Check status
  git add .                  Stage changes
  git commit -m              Commit
  git log                    History
  git branch                 List branches
  git switch -c              Create & switch branch
  git switch                 Switch branch
  git merge                  Merge branch
  git push                   Upload changes
  git pull                   Download & merge changes
  git fetch                  Download only
  git remote -v              View remote
  git branch -d              Delete local branch
  git push origin --delete   Delete remote branch

------------------------------------------------------------------------

# Real Company Workflow

``` text
main
│
├── feature-login
├── feature-dark-mode
├── feature-history
└── bugfix-divide-zero
```

Each feature is developed in its own branch and merged into `main` after
testing.
