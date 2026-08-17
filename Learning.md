# 🚀 Git & GitHub Cheat Sheet

> **Git** is a Distributed Version Control System. **GitHub** is a web platform built on top of Git for hosting repositories and collaboration.

---

## 📌 1. Git Basics

- 🔍 Tracks changes in files
- 🤝 Allows teamwork
- 💻 Every developer has a local copy (repository)
- ✈️ Works offline
- 🕘 Maintains history

---

## 🔄 2. Git Workflow

The four stages a file moves through:

```
Working Directory  →  Staging Area  →  Local Repository  →  Remote Repository
```

| Stage                    | What Happens Here        |
| ------------------------ | ------------------------ |
| 🗂️ **Working Directory** | You edit files here      |
| 📥 **Staging Area**      | You add changes here     |
| 💾 **Local Repository**  | Changes committed here   |
| ☁️ **Remote Repository** | Pushed to GitHub (cloud) |

---

## ⚔️ 3. Git vs GitHub

|                | 🖥️ Git                   | 🌐 GitHub             |
| -------------- | ------------------------ | --------------------- |
| **What it is** | Command Line Tool        | Web Platform          |
| **Purpose**    | Used for version control | Hosting Git repos     |
| **Access**     | Works locally            | Works in cloud        |
| **Function**   | Tracks changes           | Enables collaboration |
| **Created by** | By Linus Torvalds        | Owned by Microsoft    |

---

## ⌨️ 4. Important Git Commands

| Command               | Description                   |
| --------------------- | ----------------------------- |
| `git init`            | Initialize a new repository   |
| `git clone <url>`     | Clone a repository            |
| `git status`          | Show current status           |
| `git add <file>`      | Add file to staging area      |
| `git add .`           | Add all files to staging area |
| `git commit -m "msg"` | Commit changes with a message |
| `git log`             | Show commit history           |
| `git branch`          | List all branches             |
| `git branch <name>`   | Create a new branch           |
| `git checkout <name>` | Switch to a branch            |
| `git merge <name>`    | Merge branch into current     |
| `git pull`            | Fetch and merge from remote   |
| `git push`            | Push changes to remote repo   |
| `git remote -v`       | Show remote repositories      |

---

## 🧭 5. Basic Git Command Flow

```
1️⃣  Make changes in Working Directory
        ↓
2️⃣  Move to Staging Area        →   git add <file>
        ↓
3️⃣  Save to Local Repo          →   git commit -m "message"
        ↓
4️⃣  Send to Remote Repo         →   git push origin <branch>
```

---

## 🌿 6. Git Branching

- 🌱 Branching allows you to work on features independently
- 🏠 Main branch is usually `main` or `master`
- 🔀 After changes, merge branch into main

```
main
  └── feature-1
```

### 🌳 Every Branching Command You Need to Know

| Command                                      | Description                                               |
| -------------------------------------------- | --------------------------------------------------------- |
| `git branch`                                 | List all local branches (current branch is highlighted)   |
| `git branch -a`                              | List **all** branches, local and remote                   |
| `git branch -r`                              | List remote-tracking branches only                        |
| `git branch <name>`                          | Create a new branch (doesn't switch to it)                |
| `git checkout <name>`                        | Switch to an existing branch                              |
| `git checkout -b <name>`                     | Create a new branch **and** switch to it                  |
| `git switch <name>`                          | Switch to an existing branch (modern alternative)         |
| `git switch -c <name>`                       | Create a new branch and switch to it (modern alternative) |
| `git branch -m <old> <new>`                  | Rename a branch                                           |
| `git branch -d <name>`                       | Delete a branch (safe — blocks if unmerged)               |
| `git branch -D <name>`                       | Force-delete a branch (even if unmerged)                  |
| `git push origin --delete <name>`            | Delete a branch on the remote                             |
| `git merge <name>`                           | Merge `<name>` into the current branch                    |
| `git merge --no-ff <name>`                   | Merge and always create a merge commit                    |
| `git merge --abort`                          | Abort a merge that has conflicts                          |
| `git rebase <name>`                          | Reapply current branch's commits on top of `<name>`       |
| `git rebase --continue`                      | Continue a rebase after resolving conflicts               |
| `git rebase --abort`                         | Cancel an in-progress rebase                              |
| `git cherry-pick <commit>`                   | Apply a specific commit from another branch               |
| `git branch --merged`                        | Show branches already merged into current                 |
| `git branch --no-merged`                     | Show branches **not yet** merged into current             |
| `git log --oneline --graph --all`            | Visualize branch history as a graph                       |
| `git push -u origin <name>`                  | Push a new branch and set upstream tracking               |
| `git branch --set-upstream-to=origin/<name>` | Link an existing local branch to a remote branch          |

> 💡 **Tip:** `git switch` and `git checkout` do similar jobs, but `switch` is newer and safer — it's dedicated purely to changing branches, while `checkout` is older and also used for restoring files.

---

## 🙈 7. `.gitignore`

- Used to ignore files/folders in a repository
- Create a file named `.gitignore` in the root
- Add patterns of files/folders to ignore

```gitignore
# Ignore log files
*.log

# Ignore node_modules
node_modules/

# Ignore env files
.env

# Ignore OS files
.DS_Store
Thumbs.db
```

---

## 🐙 8. GitHub Basics

- 📦 Create repository
- ⬆️ Push code
- 🤝 Collaborate with others
- 🐞 Create Issues
- 🔁 Do Pull Requests
- ✅ Review & Merge

---

## 🔗 9. GitHub Workflow

| Step                     | Action                                    |
| ------------------------ | ----------------------------------------- |
| 📁 **Create Repository** | Create a new repository on GitHub         |
| 📤 **Push Code**         | Push your local code to GitHub            |
| 👥 **Invite Others**     | Collaborate with your team                |
| ↗️ **Pull Request**      | Create a PR for changes and discussion    |
| ✔️ **Review & Merge**    | Review changes and merge into main branch |

---

## 🛟 10. Common Git Scenarios

| Scenario                                | Command                         |
| --------------------------------------- | ------------------------------- |
| ↩️ Undo last commit (keep changes)      | `git reset --soft HEAD~1`       |
| 🗑️ Undo last commit (delete changes)    | `git reset --hard HEAD~1`       |
| 📤 Unstage a file                       | `git reset <file>`              |
| 🚫 Discard changes in working directory | `git checkout -- <file>`        |
| 📦 Stash changes temporarily            | `git stash` / `git stash apply` |

---

## 📖 11. Git Command Cheat Sheet

<table>
<tr>
<th>⚙️ Setup</th>
<th>🧱 Basic</th>
<th>🌿 Branching & Merging</th>
<th>☁️ Remote</th>
<th>🧰 Others</th>
</tr>
<tr valign="top">
<td>

```bash
git config --global \
  user.name "Name"
git config --global \
  user.email "email"
```

</td>
<td>

```bash
git init
git status
git add .
git commit -m "message"
git log --oneline
git diff
```

</td>
<td>

```bash
git branch
git branch <name>
git checkout <name>
git checkout -b <name>
git merge <name>
git branch -d <name>
```

</td>
<td>

```bash
git remote add origin <url>
git remote -v
git push -u origin <branch>
git pull origin <branch>
git fetch
```

</td>
<td>

```bash
git stash
git stash pop
git tag <tagname>
git tag
git show <commit/tag>
```

</td>
</tr>
</table>

---

## 🏆 12. Advantages

- ✅ Version control & history tracking
- ✅ Collaboration made easy
- ✅ Backup & recovery
- ✅ Branching for experimentation
- ✅ Open source & community support

---

## ⭐ 13. Best Practices

- ⭐ Commit small and meaningful changes
- ⭐ Write clear commit messages
- ⭐ Pull before push
- ⭐ Use branches for new features
- ⭐ Review code before merging

---

## 🔑 14. Key Terms

| Term              | Meaning                            |
| ----------------- | ---------------------------------- |
| 📦 **Repository** | Storage of project and its history |
| 💾 **Commit**     | Save point in history              |
| 🌿 **Branch**     | Independent line of development    |
| 🔀 **Merge**      | Combine changes from branches      |
| 📋 **Clone**      | Copy of repository                 |
| ⬇️ **Pull**       | Fetch + Merge from remote          |
| ⬆️ **Push**       | Send changes to remote             |

---

## 💡 15. Short Tips

- ⬆️ Always pull before push
- ✅ Commit often
- 💬 Use meaningful messages
- 🛡️ Keep `.gitignore` updated
- 👀 Review before merging

---

<div align="center">

**Made with 🖤 (love) for developers who git it 😄**

</div>
