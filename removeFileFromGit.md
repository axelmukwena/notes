### How to remove a file from Git

    $ find . -name FILENAME -print0 | xargs -0 git rm -f --ignore-unmatch
    
Add file to `.gitignore`
