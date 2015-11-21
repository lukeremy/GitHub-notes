---
title: "Git Bash / GitHub notes"
author: "Luke Remy"
date: "Friday, January 09, 2015"
output: pdf_document
---
_________________________________________________

[Simple Guide to forks in GitHub and Git](http://www.dataschool.io/simple-guide-to-forks-in-github-and-git/)  
_________________________________________________

**Cloning repos to your computer**  

*1. Set working directory in Git Bash:*   

$ cd ~/Desktop/    

*2. Copy hyperlink from GitHub, use insert button to clone into Git Bash:*    

$ git clone https://github.com/lukeremy/test  

*3. Navigate to new folder created in working directory(with same name as GitHub repo), look at files:*  

$ cd test   
$ ls

*4. Check on remotes (references to repos that are not on computer):*

$ git remote -v

*5. If origin remote is not present, add one (using GitHub repo url):*

$ git remote add origin https://github.com/lukeremy/test

*6. Edit existing file (README.md) in test repo:*

Open README.md file in any text editor (e.g., Notepad).
Make any desired edits, save, and close.

*7. Create new markdown file:*

$ touch new.md

*8. Open and edit new markdown file:*

Open new.md file in text editor, make edits, save, and close.

*9. Check status of files:*

$ git status

*10. Change status of files for committing to GitHub:*

Add one file at a time:
$ git add new.md

Add all files at once:
$ git add .

*11. Check status of files again to verify that they are ready for commit:*

$ git status

*12. Commit files:*

     *Option A, using insert mode:*

     $ git commit (this will open a new window)
     type your comment at the top of the new window
     hit ESC, then ":wq" in the field below
     
     *Option B, adding argument with -m "text":*

     $ git commit -m "edit readme and added new"

*13. Now that commit is complete, re-check status to confirm there is nothing left to commit:*

$ git status

*14. Push these changes to GitHub, refresh GitHub to verify that repo has been modified:*

$ git push origin master

______________________________________________________________________________

**Syncing your GitHub fork**  

*1. Copy hyperlink of original repo, add to your remotes, then check that it worked:*

$ git remote -v  
$ git remote add upstream <github url>  
$ git remote -v  

*2. Fetch changes:*

$ git fetch upstream

*3. Merge changes:*

$ git merge upstream/master

*4. Push changes to GitHub so that your repo is in snyc:*

$ git push origin master















  
