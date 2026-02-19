# Git Test Documentation - Hafsa Naveed

## Commands Log 


### Clone the repository to start the test     
- git clone https://github.com/Gushtasp47/Minutes-of-meetings-App.git 

### Enter the cloned repo directory
- cd Minutes-of-meetings-App     

### Create and switch to personal branch
- git checkout -b hafsanaveed      

### Create personal directory
- mkdir hafsanaveed       

### For documenting all steps    
- Created process.md with initial header 

### commit process.md
git add hafsanaveed/process.md
git commit -m "Initial setup: create personal directory and process.md"

### Create secondary branch for conflict simulation (Phase 1)
- git checkout -b hafsanaveed-feature

### Add changes and commit on hafsanaveed-feature
- git add hafsanaveed/process.md
- git commit -m "Phase 1: modify process.md on feature branch"

### Switch back to personal branch
- git checkout hafsanaveed

### Add changes and commit on hafsanaveed
- git add hafsanaveed/process.md
- git commit -m "Phase 1: modify process.md on hafsanaveed branch"


### Rebase branch
- git rebase hafsanaveed-feature
- git add hafsanaveed/process.md
- git rebase --continue

### Show compact visual history after rebase
- git log --oneline --graph --decorate --all


### Create and commit .env file by mistake
- git add hafsanaveed/.env
- git commit -m "Phase 2: accidentally add .env"


### Untrack .env, add to gitignore and amend previous commit to remove .env
- git rm --cached hafsanaveed/.env
- echo .env > .gitignore
- git add .gitignore
- git commit --amend --no-edit


### Squash last 3 commits in 1
- git rebase -i HEAD~3
In editor: change to
pick first
squash second
squash third


### Reword Older commit
- git rebase -i HEAD~5
In editor: change to
pick first
pick second
pick third
reword forth
pick fifth


### Remove Older commit
- git rebase -i HEAD~6
In editor: change to
pick first
pick second
pick third
pick forth
pick fifth
drop sixth

###  Push branch to origin
- git push origin hafsanaveed

### Add Local commit
git add hafsanaveed/process.md
git commit -m "Phase 4: new local commit"

