# Assignment 1.5 — Solution: GitHub Essentials II

## 1. Create / use a GitHub account
Go to https://github.com → **Sign up** (or **Sign in** if you already have one). Use the same email configured in Git (`git config user.email`).

## 2. Create a new public repository
1. Click **+** (top-right) → **New repository**.
2. **Repository name:** e.g. `github-practice`.
3. **Visibility:** select **Public**.
4. Leave *Add a README*, *.gitignore* and *license* **unchecked** (the local project already exists).
5. Click **Create repository**.

## 3. Connect the local repository to the remote
Inside your local project folder (already a Git repo with at least one commit — see Assignment 1.4):
```bash
git remote add origin https://github.com/<your-username>/github-practice.git
git remote -v                      # verify the remote URL
```

## 4. Upload files using `git push`
```bash
git branch -M main                 # make sure the branch is called main
git push -u origin main
```
> GitHub does not accept account passwords for pushes. When prompted, sign in through the browser window (Git Credential Manager) or use a **Personal Access Token** (GitHub → Settings → Developer settings → Personal access tokens) as the password.

## 5. Add a new file and push the second commit
```bash
echo "# GitHub Practice" > README.md      # or create any new file (e.g. about.html)
git status
git add README.md
git commit -m "Add README file"
git push
```

## 6. Verify the commit history on GitHub
1. Open `https://github.com/<your-username>/github-practice`.
2. Confirm the files are listed.
3. Click the **"X Commits"** link (above the file list) to see the commit history, including your first commit and "Add README file".

You can also compare with the local history:
```bash
git log --oneline
```

## Command Summary
| Command | Purpose |
|---------|---------|
| `git remote add origin <url>` | Link local repo to GitHub |
| `git remote -v` | Show configured remotes |
| `git branch -M main` | Rename current branch to `main` |
| `git push -u origin main` | First push; sets upstream |
| `git push` | Push later commits |

## Submission
🔗 Link to the public repository:

```
https://github.com/<your-username>/github-practice
```
(Replace `<your-username>` with your GitHub username, e.g. `https://github.com/larsondroidek-code/github-practice`.)
