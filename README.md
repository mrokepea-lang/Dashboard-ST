# How to Push Code to Git: A Beginner's Guide

Git is a tool that tracks changes to your code over time. Pushing code means uploading your local changes to a remote repository (like GitHub) so others can see them.

---

## Prerequisites

- Git installed on your computer — download it at https://git-scm.com
- A GitHub account (or another Git hosting service)
- A repository already created on GitHub

---

## Step 1: Configure Git (First Time Only)

Before you do anything else, tell Git who you are. Open your terminal and run:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

You only need to do this once per computer.

---

## Step 2: Clone the Repository (If Starting Fresh)

If you don't have the project on your computer yet, download it:

```bash
git clone https://github.com/your-username/your-repo-name.git
```

Then navigate into the project folder:

```bash
cd your-repo-name
```

If you already have the project folder locally, skip this step.

---

## Step 3: Check the Current Status

Before making changes, check what state your files are in:

```bash
git status
```

This shows you which files have been modified, added, or deleted. Files in red have changes that haven't been staged yet.

---

## Step 4: Stage Your Changes

Staging means selecting which changes you want to include in your next save point (called a "commit").

To stage a specific file:

```bash
git add filename.txt
```

To stage all changed files at once:

```bash
git add .
```

Run `git status` again — staged files will now appear in green.

---

## Step 5: Commit Your Changes

A commit is a snapshot of your staged changes, saved with a message describing what you did.

```bash
git commit -m "Add login page and update navigation"
```

Tips for a good commit message:
- Keep it short (under 72 characters)
- Use present tense: "Add feature" not "Added feature"
- Describe *what* changed and *why*, not *how*

---

## Step 6: Push Your Changes

Now upload your commit to the remote repository:

```bash
git push
```

If this is your first push on a new branch, Git may ask you to set the upstream:

```bash
git push -u origin main
```

After this one-time setup, `git push` alone will work for future pushes.

---

## Step 7: Verify on GitHub

Open your repository on GitHub in a browser. You should see your latest commit message at the top of the file list, confirming your code was pushed successfully.

---

## Quick Reference

| Command | What It Does |
|---|---|
| `git status` | Show which files have changes |
| `git add .` | Stage all changes |
| `git add <file>` | Stage a specific file |
| `git commit -m "message"` | Save staged changes with a description |
| `git push` | Upload commits to GitHub |
| `git pull` | Download the latest changes from GitHub |

---

## Common Issues

**"Permission denied" when pushing**
You may need to authenticate. GitHub requires a Personal Access Token instead of a password — create one at GitHub Settings > Developer Settings > Personal Access Tokens.

**"Your branch is behind the remote"**
Someone else pushed changes before you. Run `git pull` first to download their changes, then push yours.

**Pushed the wrong thing?**
Don't panic. Ask a teammate or search "git revert" — Git is designed to recover from mistakes.
