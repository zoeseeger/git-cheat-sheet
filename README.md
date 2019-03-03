## Git commands

#### Create a repository:

Move to folder where the repository will be stored with files that will be uploaded.
    cd folder-with-files-to-put-in-repository
Initialise a git repository. This will create a .git folder in the current directory where all of the information about this repository will be stored.

    git init
    
Create the file README where the information about the files to the user can be written.

    touch README
    
Add everything in current directory and subdirectories to the repository.

    git add .
    
'commit' will find changes between last version of the repository and the current one and track these changes. The commit is saved with a comment given by the editor that breifly explains what the changes are.

    git commit -m "Initial commit"
    
'push' uploads all of the changes stored from the 'commit' command to the github site where it is stored and changes are tracked. The main 'branch' of the project is called the master. When different people work on code at the same time they can generate different branches that can later be merged back to the master branch or rejected if they do not work well with the rest of the changed code.

    git push -u origin master

Branches are a good way to fix bugs in code as they track differences between old and new versions so that if a new version is distributed only the buggy parts of the code need to be changed and the client does not need to redownload or install the whole source material. Git will take care of the changes.

#### Updating repository on git:

    git add .
    git commit -m <Comment on changes made>
    git push

#### Updating local repository from git:

    git pull

#### Add submodule to git repository:

Clones repository to specified path and adds .gitmodules in root of repository.

    git submodule add <url-to-github-repository> <local-path-to-bundle>
    git add . 
    git commit -m <Comment on update>

#### Synchronise all submodules:
    
    git submodule init 
    git submodule update

