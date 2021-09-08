# Git

## Setup

```bash
# Check git version
git --version

# Set username and email
git config --global user.name "Your Name"
git config --global user.email "youremail@mail.com"

# Set default branch as main
git config --global init.defaultBranch main

# Set automatic command line colouring for git
git config --global color.ui auto

# List all global git config variables
git config --list

# ssh setup
# Add id_ed25519.pub as ssh key on Github
# Path in Linux : ~/.ssh/id_ed25519.pub
# Path in Windows : /c/Users/you/.ssh/id_ed25519.pub
ssh-keygen -t ed25519 -C "youremail@mail.com"

# OR

# Store credentials
git config --global credential.helper store
```

## Start

```bash
# Create a local git repository
cd [path]
git init
```

## Stage and Snapshot

```bash
# Check the status of a repository. (View unstaged, staged and modified files)
git status

# Add a file from working area to staging area
git add [path]

# Create a snapshot of your staged changes
git commit -m "[descriptive message]"

# Change the commit message of last commit
git commit --amend -m "[new message]"

# Display the difference of what is changed but not staged 
git diff

# Display the difference of what is staged but not commited
git diff --staged

# Unstage a file while retaining the changes in working directory
git reset [file]
```

## Branch & Merge

```bash
# List your branches
git branch

# Create a new branch at the current commit
git branch [branch_name]

# Switch to another branch
git checkout [branch_name]

# Create and swtich to the branch
git checkout -b [branch_name]

# Merge the specified branch's history into the current one
git merge [branch_name]

# Show commit history of current branch
git log
```

## Remote repositories

```bash
# Clone a remote repository
git clone [url]

# Fetch the meta-data of remote repository
git fetch

# Transmit local changes to remote repository
git push

# Fetch and merge any commits from the remote branch
git pull
```

## Rewrite history

```bash
# Apply commits of current branch ahead of specified one
git rebase [branch_name]

# Reset to a specified commit and clear the staging area
git reset --hard [commit]

# Reset to a specified commit without clearing the staging area
git reset --soft [commit]
```

## Ignoring patterns

```bash
# Add files that you want to ignore in .gitignore file
*.txt
node_modules
```

## Temporary commits

```bash
# Save modified and staged changes
git stash

# List stashes
git stash list

# Apply changes from top stash stack
git stash apply

# Drop changes from top stash stack
git stash drop

# Apply and drop from top stash stack
git stash pop
```

---

# Extras

![01_git_and_git_log .jpeg](Git%20d4421e291d8540629eba660964d4fc71/01_git_and_git_log_.jpeg)

![02_git_pull.jpeg](Git%20d4421e291d8540629eba660964d4fc71/02_git_pull.jpeg)

![03_git_push.jpeg](Git%20d4421e291d8540629eba660964d4fc71/03_git_push.jpeg)

![04_merge_and_rebase.png](Git%20d4421e291d8540629eba660964d4fc71/04_merge_and_rebase.png)
