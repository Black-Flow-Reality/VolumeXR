
# VolumeXR

#### Assignees: Clark + Albert

#### To-do:
- Create documentation
- Build the design of VolumeXR - interface/UI
- Creation of project - scanning of 3D environment / placement of 3D objects
- Downloading and categorizing 3D models

### Languages / Tools used:
- Godot as game engine
- Blender as 3D modeling/shader/texture software
- Affinity - textures/shaders

### Minimum Viable Product:
- pre-downloaded 3D assets, categorized through tags
- scan the room and convert to a 3D environment -> phone
- hosted on a computer

### Post MVP:
- allow for co-op environments -> peer to peer connection
- allow for superposition of real environment / 3D environment
- scanning in multiple steps (placement of light source, etc)
- connection to external apps / other multi modal media

---

## 🛠️ Onboarding: Git & GitHub Setup Guide

Welcome to the team! If you are new to Git and version control, follow this step-by-step guide to set up your environment and learn how to share your code with the team.

### Step 1: Configure Your Local Git Account
Before you make any changes, you need to tell Git who you are. This ensures your commits are properly attributed to you.

1. Open your terminal (Mac/Linux) or Command Prompt/Git Bash (Windows).
2. Set your name and email by running the following commands (replace the text inside the quotes with your actual information):
   ```bash
   git config --global user.name "Your First and Last Name"
   git config --global user.email "your_email@example.com"

```

*Note: Use the same email address you used to create your GitHub account.*

### Step 2: Log In to GitHub via CLI (`gh auth login`)

Instead of messing with complicated Personal Access Tokens (PATs) or SSH keys, we use the official **GitHub CLI** tool to log in securely.

1. Make sure you have downloaded and installed the GitHub CLI (`gh`).
2. In your terminal, type the following command and press Enter:
```bash
gh auth login

```


3. Use your arrow keys and Enter key to answer the prompts exactly like this:
* **What account do you want to log into?** `GitHub.com`
* **What is your preferred protocol for Git operations on this host?** `HTTPS`
* **Authenticate Git with your GitHub credentials?** `Yes`
* **How would you like to authenticate GitHub CLI?** `Login with a web browser`


4. A **one-time activation code** (8 characters) will appear in your terminal. Copy it.
5. Press **Enter** to open your browser automatically. Paste the code into the GitHub prompt, then click **Authorize github**.

Once the terminal says you are logged in, you are good to go!

---

## 🔄 Daily Workflow: Syncing Your Code

When working with Godot scenes, scripts, or Blender assets, you need to constantly pull your teammates' changes and push your own. Here is the daily workflow order:

### 1. Fetch & Pull (Do this BEFORE you start working)

Always get the latest code from your team before you begin editing files. This prevents merge conflicts later.

* **`git fetch`** checks the GitHub repository to see if anyone has uploaded new work, without touching your local files:
```bash
git fetch origin

```


* **`git pull`** downloads those changes and merges them directly into your local workspace:
```bash
git pull origin main

```



### 2. Add & Commit (Do this when you finish a task)

Once you have created or edited a file (like designing a UI element or adding a 3D model), save a "snapshot" of your progress locally.

* **`git add`** tells Git which files you want to include in your next snapshot.
```bash
# To add a specific file:
git add path/to/file.gd

# To add ALL changed and new files at once:
git add .

```


* **`git commit`** locks in your snapshot with a required description of what you did. Keep messages short and meaningful!
```bash
git commit -m "Add basic UI interface for asset selection"

```



### 3. Push (Do this to share your work)

Right now, your commit only exists on your own computer. To upload it to GitHub so Clark, Albert, and the rest of the team can see it, use push.

* **`git push`** sends your committed changes to the cloud:
```bash
git push origin main

```



### ⚠️ Quick Tip for Godot Engine

Before you run `git add` or `git commit`, make sure to **Save All Scenes** in the Godot Editor (`Ctrl + Shift + S` or `Cmd + Shift + S`). Godot dynamically updates `.tscn` text files when you save, so committing without saving might leave out your actual scene modifications!