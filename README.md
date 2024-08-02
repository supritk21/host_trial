to host react app on git hub using gh-pages
run below command on vs code terminal
 ```
 gh-pages --save-dev
 ```
  then create the github repository and then execute below commands on vs code terminal.

  ```
git init
git add . 
git status
```

git init \
Initializes a new Git repository in the current directory. \
Creates a hidden .git directory that stores all the necessary files for version control. \
you can start tracking changes to your files using Git. \

git add . 
Stages (prepares) all changes in the current directory for the next commit. \
The . represents all files and directories in the current location. \
Use this command when you want to include all changes in your next commit. 

git status 
Displays the current status of your working directory and staging area. \
Shows which files are modified, staged, or untracked. \
Useful for checking what changes are ready to be committed.

then run below git command
```
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/username/repo-name.git
git push -u origin main
```
1. git commit -m "first commit"
Commits the staged changes to the local Git repository.
The -m flag allows you to provide a commit message (in this case, “first commit”) to describe the changes made in this commit.
Committing creates a snapshot of your project at that point in time.
2. git branch -M main
Renames the default branch from the previous name (usually “master”) to “main.”
This command ensures that your repository uses the more inclusive term “main” as the default branch name.
3. git remote add origin https://github.com/username/repo-name.git
Associates your local Git repository with a remote repository hosted on GitHub (or any other Git hosting service).
The origin is a common name for the remote repository.
Replace https://github.com/username/repo-name.git with the actual URL of your remote repository.
4. git push -u origin main
Pushes your local commits to the remote repository (in this case, the “main” branch).
The -u flag sets up tracking so that future git push commands without specifying a branch will automatically push to the same branch on the remote repository.

then add homepage and add below code in script
```
add below in package.json
 "homepage": "https://user_name.github.io/repo_name"
```
add below code in script
```
"predeploy":"npm run build",
"deploy" :"gh-pages -d build",
```

react app will be deployed to github use below link replace username and repo name with your github profile name and github repo name respectively.
```
https://user_name.github.io/repo_name
```
