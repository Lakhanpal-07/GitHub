# GitHub
A practical repository showcasing Git fundamentals and GitHub workflows. Includes examples of commits, branching, merging, and remote collaboration. Designed for engineers learning version control and DevOps practices. This repo demonstrates how to manage code history, resolve conflicts, and push projects to GitHub with clarity and efficiency.


# Git & GitHub Commands Cheat Sheet

Complete guide to day-to-day Git and GitHub commands used in real production environments for DevOps, cloud, and software development teams.[1][2]

## Top Git Commands

### 1. Initialize repository
```bash
git init
```
Creates a new Git repository in the current directory.[1]

### 2. Clone repository
```bash
git clone https://github.com/username/repo.git
```
Downloads a remote repository to your local machine.[1]

### 3. Check status
```bash
git status
```
Shows modified, staged, and untracked files.[3][1]

### 4. Add files
```bash
git add .
git add filename.txt
git add -A
```
Stages all files, a specific file, or all tracked changes including deletions.[3][2]

### 5. Commit changes
```bash
git commit -m "feat: add new feature"
git commit -m "fix: resolve bug in login"
git commit -m "docs: update README"
```
Saves staged changes with a descriptive message.[4][5]

### 6. View history
```bash
git log
git log --oneline
git log --graph
git log -n 5
```
Shows commit history in full, compact, graph, or limited form.[3][6]

### 7. Check branches
```bash
git branch
git branch -a
git branch --show-current
```
Lists local branches, all branches, or only the current branch.[6][2]

### 8. Create branch
```bash
git branch feature-name
git checkout -b feature-name
git switch -c feature-name
```
Creates a new branch, or creates and switches to it.[3][6]

### 9. Switch branch
```bash
git checkout main
git checkout feature-name
git switch main
```
Moves from one branch to another.[3][6]

### 10. Fetch from remote
```bash
git fetch origin
git fetch --all
```
Downloads remote changes without merging them into the current branch.[7][8]

### 11. Pull changes
```bash
git pull origin main
git pull --rebase origin main
```
Updates the local branch with remote changes; `--rebase` keeps a cleaner, linear history.[7][9]

### 12. Push changes
```bash
git push origin main
git push origin feature-name
git push -u origin main
git push --force
```
Uploads local commits to the remote repository; `--force` should be used carefully.[7][1]

### 13. Show remotes
```bash
git remote -v
git remote add origin URL
git remote remove origin
```
Displays, adds, or removes remote repository connections.[1]

### 14. Check diff
```bash
git diff
git diff --staged
git diff main feature
```
Shows unstaged changes, staged changes, or differences between branches.[3][6]

### 15. Restore or unstage changes
```bash
git checkout -- filename.txt
git restore filename.txt
git restore --staged filename.txt
```
Discards local changes or removes files from the staging area.[6]

### 16. Merge branch
```bash
git checkout main
git merge feature-name
```
Combines changes from one branch into another.[10][11]

### 17. Delete branch
```bash
git branch -d feature-name
git branch -D feature-name
git push origin --delete feature-name
```
Deletes local or remote branches after they are no longer needed.[2]

### 18. Stash changes
```bash
git stash
git stash list
git stash pop
git stash drop
```
Temporarily saves uncommitted changes and restores or removes them later.[12]

### 19. Show commit details
```bash
git show commit-hash
git show HEAD
```
Displays detailed information about a specific commit or the latest commit.[6]

### 20. Reset commits
```bash
git reset --soft HEAD~1
git reset --hard HEAD~1
```
Moves the branch pointer backward while keeping or discarding changes.[6]

## GitHub CLI Commands

### 21. Create pull request
```bash
gh pr create -t "Title" -b "Description"
```
Creates a pull request from the terminal.[1]

### 22. View pull requests
```bash
gh pr list
gh pr view 123
```
Lists pull requests or shows details for one pull request.[1]

### 23. Fork repository
```bash
gh repo fork
```
Creates a fork of the current repository under your GitHub account.[1]

## Production Workflow Example

```bash
# Start the day by syncing
git fetch origin
git pull --rebase origin main

# Create a feature branch
git checkout -b feature/new-feature

# Make changes, then stage and commit
git add .
git commit -m "feat: implement new feature"

# Push branch to GitHub
git push -u origin feature/new-feature
```
This workflow is widely used because it syncs first, isolates changes in a feature branch, and keeps history cleaner with rebase.[7][9][5]

## Best Practices

- Commit often with small, focused changes.[4][5]
- Use clear commit messages like `feat:`, `fix:`, `docs:`, and `chore:`.[5]
- Pull before pushing to avoid conflicts.[7]
- Use feature branches instead of committing directly to `main`.[13][5]
- Prefer pull requests for review and controlled merges.[5][1]
- Use `git pull --rebase` when your team prefers a linear history.[9][11]
