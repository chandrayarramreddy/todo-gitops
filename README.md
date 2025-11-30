To Create Repo from CMD instead of using GIT GUI/WebPage, Below are commands used

# 1. Install GitHub CLI
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt install gh -y

# 2. Login
gh auth login  # GitHub username → Authenticate

# 3. Create repo + push (ONE COMMAND)
mkdir todo-gitops && cd todo-gitops
git init
echo "# Todo GitOps Project" > README.md
git add . && git commit -m "Initial commit"
gh repo create todo-gitops --public --push --source=.  # Creates + pushes!



fixes

git remote -v


if url found no issue


git remote set-url origin https://github.com/chandrayarramreddy/todo-gitops.git
git remote -v  # Verify new URL


remove and assign

git remote remove origin
git remote add origin https://github.com/chandrayarramreddy/todo-gitops.git
git remote -v  # Verify


branch creation

git branch -M main
git push -u origin main


competed check

# 1. Check current state
git status
git remote -v
git log --oneline -3

# 2. Fix origin (choose ONE)
git remote set-url origin https://github.com/chandrayarramreddy/todo-gitops.git
# OR
# git remote remove origin && git remote add origin https://github.com/chandrayarramreddy/todo-gitops.git

# 3. Push
git push -u origin main

# 4. Verify on GitHub
echo "✅ Repo: https://github.com/chandrayarramreddy/todo-gitops"


