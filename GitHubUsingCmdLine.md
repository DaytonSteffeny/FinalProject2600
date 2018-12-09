## Git and GitHub Using Command Line - Condensed

This document presents Git and GitHub using the command line in a condensed format. The following video demonstrates the 

process.
Git and GitHub Using the Command Line, 32:15
## Create a local project directory with files in it
## Create a repository on GitHub with README and .gitignore (with .DS_Store added)
## Setup local repository
  _git init_
  _git add ._
  _git commit -m "First commit"_
  _git remote add origin <GitHub_remote_repository_clone_https_url>_
  _git pull --rebase origin master_
  _git rm -r --cached ._
  _git add ._
  _git commit -m "Applied .gitignore"_
  _git push -u origin master_
## Add a feature to an application
Create a branch for the feature.
  _git branch feature/<feature_descriptor>_
  _git checkout feature/<feature_descriptor>_
Write and test the code for the feature. Remember to commit and push often during the development of the feature (see below).
  _git add ._
  _git commit -m "<message describing changes>"_
  vgit push -u origin feature/<feature_descriptor>_
     
When the feature is complete, merge it into the master branch.
  _git checkout master_
  _git merge feature/<feature_descriptor>_
  _git push -u origin master_

## Fix a bug
Create a branch for the bug fix.
  _git branch bugfix/<bug_descriptor>_
  _git checkout bugfix/<bug_descriptor>_
Fix the bug and test the code. Remember to commit and push often during the coding of the bug fix (see below).
  _git add ._
  _git commit -m "<message describing changes>"_
  _git push -u origin bugfix/<bug_descriptor>_
When the bug fix is complete, merge it into the master branch.
  _git checkout master_
  _git merge bugfix/<bug_descriptor>_
  _git push -u origin master_
   
