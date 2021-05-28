## Git commands

#### Create a repository

Create a new repository on your GitHub account. To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub. Remember the name of your repository.

Move to folder where the repository will be stored with files that will be uploaded.

    cd foldername
    
Initialise a git repository. This will create a .git folder in the current directory where all of the information about this repository will be stored.

    git init
    
Create the file README where the information about the files to the user can be written.

    touch README
    
Add everything in current directory and subdirectories to the repository:

    git add .
    
OR you can choose to add specific files:

    git add filename
    
'commit' will find changes between last version of the repository and the current one and track these changes. The commit is saved with a comment given by the editor that breifly explains what the changes are.

    git commit -m "Initial commit"
 
To add your files to the repository created at the start specify the repository by the following command after inserting the correct username and name of the repository. This updates the URL in .git/config.
 
    git remote add origin https://github.com/account/name-of-your-repository.git
    
Alternatively, if your host is blocking access to the URL during the push process insead change the URL to:

    git remote add origin https://account@github.com/account/name-of-your-repository.git
    
'push' uploads all of the changes stored from the 'commit' command to the github site where it is stored and changes are tracked. The main 'branch' of the project is called the main. When different people work on code at the same time they can generate different branches that can later be merged back to the main branch or rejected if they do not work well with the rest of the changed code.

    git push -u origin main

Branches are a good way to fix bugs in code as they track differences between old and new versions so that if a new version is distributed only the buggy parts of the code need to be changed and the client does not need to redownload or install the whole source material. Git will take care of the changes.

#### Updating repository on git

    git add .
    git commit -m <Comment on changes made>
    git push
    
#### Remove files from a repository
    
Remove all files that we have previously added from our stored information:
    
    git rm -r --cached .
    
OR remove one file at a time:

    git rm <path/to/file>

If we have cleared all files from the repository we will have to add the remaining files again with:

    git add .
    git commit -m <Comment on changes made>
    git push
    
#### Check changes between local and remote repositories

Get all information from remote host:

    git fetch
    
Check remote host files again current repository:
    
    git log -p HEAD..FETCH_HEAD

#### Updating local repository from git

    git pull

#### Add submodule to git repository

Clones repository to specified path and adds .gitmodules in root of repository.

    git submodule add <url-to-github-repository> <local-path-to-bundle>
    git add . 
    git commit -m <Comment on update>

#### Synchronise all submodules
    
    git submodule init 
    git submodule update
    
#### Find differences between local and github

Suppose you've got a remote called origin that refers to your GitHub repository, you would do:

    git fetch origin
    git diff main origin/main
    
You can then merge with branch main by:

    git merge origin/main
    
#### Revert to last github commit

After you have found differences between the local and github repository, if you want to revert local changes to the github repository do:

    git reset --hard
    
### Pull last commit of one file

    git checkout file
    

