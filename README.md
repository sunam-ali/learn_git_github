# Introduction :

1. Folder Command
  - dir - How many folders and files
  - dir /a - Also Hidden folders and files
  - cd tab - Change direcoty
  - cd .. - Back from current folder
  - cls - Clear command line
  - mkdir folder_name - Create folder
  - rmdir folder_name - Delete folder
  - rmdir /s example_folder - Remove Folder and all files and subdirectory

2. File Command:
  - copy nul test.txt - Create file
  - del test.txt - Delete file
  - echo "hello world" > file_name - Edit File
  - type file_name - view file
  - copy test.txt new.txt - Copy one file to Another

3. Git Configuration Command:
  - Local (specific folder) & Global (all folder) & System [use system instead of global ]
  - git config -- list  - Check all Configuration
  - git config --global list  - Check all Configuration globally
  - git config -- user.name "sunam-ali"  - set username for current folder only
  - git config --global user.name "sunam-ali"  - set username for globally (all) folder (overwrite)
  - git config -- user.name  - Individually check
  - git config --global --unset user.name   - to unset the username/email

4. How to Communicate with git to github (2 computer) usin SSH keys
  - Generate public and private keys in Computer 1
  - Add the Public keys to Computer 2
  - Now Computer 2 can decrypt the data send from Computer 1
  - Command :
    - ssh-keygen -t rsa -C "github-email@gmail.com"
  - Now Clone github Repo with SSH key and it works fine

# Git Basics :

  - working directory  → stagging area  → local repo  → remote repo 
  - Test (git init)    → git add        → git commit  → git push
  
  1. Command
  - git init 
  - git status - check current status of files
  - git add .  - now git can track file changes (stagging area)
  - git diff   - to see where is changed
  - git restore name        - to unstagging
  - git commit -m "message" - to bring into local repo
  - git log             - history of commit
  - git log --oneline   - history of commit in one line
  - git reset --soft HEAD^     - Uncommit 
  - git reset --soft commit_id - Also Uncommit with previous commit id
  - git checkout commit_id   - To See the diffrent version of code
  - git show commit_id       - To See Details About a Commit
  - git revert commit_id     - Remove commit but history will be there 

# Github Basics :

  - git remote -v   - shows the remote along with the url
  - git remote add origin url - connect local repo to remote 
  - git branch -M main        - to rename the branch name
  - git push -u origin main   - send files
  - git pull origin           - bring files with changes from remote
  - git remote origin new     - change the name of the repo
  - .gitignore                - preventing files and info to share like push , pull operation

# git branch & merging :

  - git branch        - check how many local branch
  - git branch -r     - check remote branch
  - git branch -a     - check both remote and local branch
  - git branch dev    - create new branch call "dev" like copying a branch
  - git checkout dev  - switch to the new branch from main/master
  - git checkout main - go back to the main branch
  - git merge dev     - merge changes (2way merge/fast forward merge)
  - git branch -d dev - delete the branch 
  - BEST PRACTICE :  
  1. pull the changes first without merging and make merge in remote then again pull

# Collaboration and Contribution
  - Fork (copy in remote) → git Clone → make pull request from remote
  - Add collaborator to a git repo - Send invitation for collaborating a repo
