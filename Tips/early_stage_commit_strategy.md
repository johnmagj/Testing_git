# Git Commit Strategy Guide for Early-Stage Projects

## 1. Initial Commit
Group foundational files into one commit:
  git add README.md .gitignore LICENSE
  git commit -m "chore: initialize project with README, license, and .gitignore"

Use "chore:" to signal setup work that doesn’t affect functionality.

---

## 2. Use Feature-Based Branches
Create a new branch for each feature or task:
  git checkout -b feature/login-form

Keeps your main branch clean and production-ready.

---

## 3. Write Clear, Conventional Commit Messages
Format:
  <type>: <imperative summary>

Examples:
  feat: add user registration form
  fix: resolve crash on login
  docs: update README with setup instructions

---

## 4. Group Related Changes Together
Commit multiple files only if they serve the same purpose.

Good:
  git add login.html login.js
  git commit -m "feat: implement login form and validation"

Avoid:
  git add login.js README.md
  git commit -m "misc: update login and README"

Mixing unrelated changes makes history harder to read and revert.

---

## 5. Commit Often, But Meaningfully
- Don’t wait until everything is done.
- Avoid committing every tiny change.
- Aim for logical checkpoints.

---

## 6. Use Interactive Staging for Precision
  git add -p

Stage only the parts of files you want to commit.
Great for separating unrelated changes in the same file.

---

## 7. Rebase Before Merging (Optional for Teams)
Keeps history linear and clean:
  git pull --rebase origin main

Especially useful before merging a feature branch.

---

## 8. Squash Commits When Merging (Optional)
Use GitHub’s “Squash and merge” to combine messy commit history into one clean commit.

---

## Commit Types Cheat Sheet

feat:     A new feature
fix:      A bug fix
docs:     Documentation changes
style:    Code formatting (no logic change)
refactor: Code restructuring (no feature or fix)
test:     Adding or updating tests
chore:    Maintenance tasks (build, deps, etc.)
perf:     Performance improvements
ci:       CI/CD configuration changes