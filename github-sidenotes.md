# Push ALL branches
git push --all origin

# Back to old commit
git log --oneline
git checkout [HASHCODE] (back to head: git checkout master)
git branch [BRANCHNAME]

# Transfer git repository from local bare to github
git remote add origin https://github.com/AndreasWoe/xxx.git
git push --mirror

original https://stackoverflow.com/ answer:
-------------------------------------------
create a new github repository via the webinterface, e.g. https://github.com/bfg/frobnozzel.git

create a local bare clone of your (local) repository (in this example closing into /tmp/new-frobnozzel.git:

git clone --bare /path/to/local/repository /tmp/new-frobnozzel.git
in the newly created bare-close, change the remote to the new github repository:

cd /tmp/new-frobnozzel.git
git remote set-url origin git@github.com:bfg/frobnozzel.git
push your entire repository to the new remote:

cd /tmp/new-frobnozzel.git
git push --mirror origin

Source: https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository

