# Git Notes

## Working with git locally

- `git init`: initialize current folder as a git repository
- `git clone <URL>`: brings the git repo from <URL> to current folder
- `git status`: tells us what we need to know about our repository

- `git add <FILE>`: adds <FILE> to the staging area
- `git commit`: open a text editor to write commit message
   - `git commit -m "MESSAGE"`: writes MESSAGE as a commit without a text editor

- `git log`: shows the log (history) of our commits
   - `git log --oneline`: shows the shorter online commit

- `git diff`: compare current uncommited state with last known git state
   - `git diff --staged`: runs git diff betwenn the staging area and last known state
- `git diff HEAD~<NUMBER>`: compares HEAD with commit <NUMBER> ago (relative)
- `git diff <HASH>`: compares HEAD with the commit in <HASH>

- `git restore --source <HASH OR HEAD~> <FILE>`: restore file to <HASH OR HEAD~>
- `git checkout <HASH OR HEAD~> <FILE>`: restore file to <HASH OR HEAD~>
   - `git checkout <HASH OR HEAD~>`: if you forget the file, you end up the detached head state
   - `git checkout main`: go back to main
   - `git switch main`: go back to main 

## Working with remotes

- `git remote add <NAME> <URL>`: adds th <URL> as a remote with the name <NAME>
   - <NAME> is by convention called `origin`
- `git remote rm <NAME>`: removes the remote called <NAME>
- `git remote -v`: look at all the remotes you have
- `git push <WHERE> <WHAT>`: push the <WHAT> branch to <WHERE>
   - `git push origin main`
- `git pull <WHERE> <WHAT>`: pulls the <WHAT> branch in <WHERE> to local computer

