# Git Caret (^) and Tilde (~) Navigation Practice

Welcome to the **Git Caret and Tilde Navigation Practice** repo!  
This project is designed to help you understand how to navigate Git commits using **caret (`^`)** and **tilde (`~`)** symbols.

---

## 📚 What You Will Learn

- How to move back **N commits** using `HEAD~N`.
- How to move to **parent commits** using `HEAD^N`.
- The differences between caret and tilde usages.
- How to combine them (e.g., `HEAD~1^2`).
- Understanding commit relationships in branching and merging scenarios.

---

## 🛠️ How to Set Up

```bash
# Clone the repo (after you create it)
git clone https://github.com/Kirankumarvel/git-caret-tilde-practice.git
cd git-caret-tilde-practice
```

Or, if starting fresh:

```bash
# Initialize the repo
git init
cd git-caret-tilde-practice

# Create first commit
echo "Initial commit" > file.txt
git add .
git commit -m "Commit 1: Initial commit"

# Second commit
echo "Add feature A" >> file.txt
git commit -am "Commit 2: Add feature A"

# Third commit
echo "Refactor A" >> file.txt
git commit -am "Commit 3: Refactor feature A"

# Create feature branch
git checkout -b my_branch

# Fourth commit on feature branch
echo "Feature B work" >> file.txt
git commit -am "Commit 4: Feature B work"

# Merge branch back into master
git checkout master
git merge my_branch -m "Commit 5: Merge my_branch"

# See the commit history
git log --oneline --graph --all
```

---

## 🎯 Practice These Commands

Try out these Git commands to practice:

```bash
# Move 1 commit back
git checkout HEAD~1

# Move 2 commits back
git checkout HEAD~2

# Go to the first parent of HEAD (useful for merge commits)
git checkout HEAD^1

# Go to the second parent of HEAD (useful to see merged branch)
git checkout HEAD^2

# Combine tilde and caret
git checkout HEAD~1^2
```

---

## 📋 Visual Reference

```text
*   Merge commit (HEAD)
|\
| * Commit on feature branch
|/
* Commit 3
* Commit 2
* Commit 1
```

---

## 🤝 Contributing

Feel free to fork, clone, and modify the repo to suit your practice needs.  
Pull requests for additional exercises are welcome!

---

## 📜 License

This project is free and open for learning purposes.  
No license restrictions. Practice away! 🚀

