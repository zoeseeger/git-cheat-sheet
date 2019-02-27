## Git commands

#### Created by initialisation with git:

    cd ~/.vim
    git init
    touch README
    git add .
    git commit -m "Initial commit"
    git push -u origin master

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

