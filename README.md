
# Introduction :

1. Folder Command (Windows CMD)
  - dir - List files and folders
  - dir /a - Show all files and folders, including hidden ones
  - cd folder_name - Change directory
  - Tab - Autocomplete folder or file names
  - cd .. - Go back to parent directory
  - cls - Clear command line
  - mkdir folder_name - Create folder
  - rmdir folder_name - Delete empty folder
  - rmdir /s folder_name - Remove folder and all files and subdirectories

2. File Command (Windows CMD):
  - copy nul test.txt - Create empty file
  - del test.txt - Delete file
  - echo hello world > file_name.txt - Create or overwrite file content
  - echo hello world >> file_name.txt - Append text to file
  - type file_name.txt - View file content
  - copy test.txt new.txt - Copy one file to another

3. Git Configuration Command:
  - Local (specific repository) & Global (all repositories of current user) & System (all users on computer)
  - git config --list - Check all configurations
  - git config --global --list - Check global configurations
  - git config --system --list - Check system configurations
  - git config user.name "sunam-ali" - Set username for current repository only
  - git config --global user.name "sunam-ali" - Set username globally (all repositories)
  - git config --global user.email "mdsunam360@gmail.com" - Set email globally
  - git config --get user.name - Individually check username
  - git config --get user.email - Individually check email
  - git config --global --unset user.name - Unset global username
  - git config --global --unset user.email - Unset global email
  - git config --show-origin --list - Show configuration and its file location

4. How to Communicate with GitHub using SSH keys:
  - Generate public and private keys on Computer 1
  - Add the public key to your GitHub account
  - Keep the private key securely on Computer 1
  - GitHub verifies your identity using the public key
  - Command:
    - ssh-keygen -t ed25519 -C "github-email@gmail.com"
    - type %USERPROFILE%\.ssh\id_ed25519.pub - View public key
    - ssh -T git@github.com - Test SSH connection
  - Add public key to GitHub Settings > SSH and GPG keys
  - Now clone GitHub repository using SSH URL
  - For another computer, generate a separate SSH key and add its public key to GitHub

# Git Basics :

  - Working Directory → Staging Area → Local Repository → Remote Repository
  - git init → git add → git commit → git push

  1. Command
  - git init - Initialize a new Git repository
  - git status - Check current status of files
  - git add . - Stage all changes in current directory and subdirectories
  - git diff - See unstaged changes
  - git diff --staged - See staged changes
  - git restore --staged file_name - Unstage a file (keep changes)
  - git restore file_name - Discard unstaged changes in a file
  - git commit -m "message" - Save staged changes into local repository
  - git log - Show commit history
  - git log --oneline - Show commit history in one line
  - git reset --soft HEAD^ - Undo latest commit but keep changes staged
  - git reset --soft commit_id - Move branch to a previous commit but keep changes staged
  - git checkout commit_id - View an older version (detached HEAD)
  - git show commit_id - See details about a commit
  - git revert commit_id - Reverse a commit by creating a new commit

# GitHub Basics :

  - git remote -v - Show remote names and URLs
  - git remote add origin url - Connect local repository to remote repository
  - git branch -M main - Rename current branch to main
  - git push -u origin main - Push files and set upstream tracking
  - git pull origin main - Fetch and integrate changes from remote main
  - git fetch origin - Download remote changes without merging
  - git remote rename origin new - Change the remote name
  - git remote set-url origin new_url - Change remote repository URL
  - .gitignore - File used to ignore untracked files and folders (e.g. node_modules, .env)

# Git Branch & Merging :

  - git branch - Check local branches
  - git branch -r - Check remote-tracking branches
  - git branch -a - Check both local and remote-tracking branches
  - git branch dev - Create a new branch called dev from current branch
  - git switch dev - Switch to dev branch
  - git switch main - Go back to main branch
  - git switch -c dev - Create and switch to a new branch
  - git merge dev - Merge dev into current branch
  - git branch -d dev - Delete safely merged local branch
  - BEST PRACTICE :
  1. Pull the latest changes from remote main
  2. Create a feature branch and work on it
  3. Commit and push your changes
  4. Create a Pull Request on GitHub
  5. Merge the Pull Request into main
  6. Pull the updated main branch to your computer

# Collaboration and Contribution

  - Fork (copy repository to your GitHub account) → Clone → Create branch → Make changes → Commit → Push → Pull Request
  - Add collaborator to a GitHub repository - Send invitation to another GitHub user
  - Collaborator accepts invitation and can contribute according to assigned permissions
