# Git & GitHub Commands Cheat Sheet

## Setup & Configuration
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
git config --global core.editor "code --wait"
git config --list

## Create & Initialize Repositories
git init
git clone <repo-url>
git remote add origin <repo-url>
git remote -v

## Basic Snapshotting (Staging & Committing)
git status
git add <file>
git add .
git reset <file>
git diff
git diff --staged
git commit -m "Commit message"
git commit -am "Message"

## Branching & Merging
git branch
git branch <branch-name>
git checkout <branch-name>
git checkout -b <branch-name>
git merge <branch-name>
git branch -d <branch-name>
git branch -D <branch-name>
git switch <branch-name>
git switch -c <branch-name>

## Remote Repositories
git remote show origin
git fetch origin
git pull origin main
git push origin main
git push -u origin main
git push --all
git push --tags

## Viewing History
git log
git log --oneline
git log --graph --oneline --all
git show <commit-id>
git blame <file>

## Undoing Changes
git restore <file>
git checkout -- <file>
git reset <commit>
git reset --hard <commit>
git revert <commit>
git clean -fd

## Tags
git tag
git tag <tag-name>
git tag -a <tag-name> -m "Message"
git push origin <tag-name>
git push origin --tags
git tag -d <tag-name>
git push origin :refs/tags/<tag>

## Stashing (Temporary Saving)
git stash
git stash list
git stash apply
git stash pop
git stash drop

## Collaboration (Forks & PRs)
git remote add upstream <original-repo-url>
git fetch upstream
git merge upstream/main
git pull upstream main

## Authentication & SSH
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub

## Advanced Commands
git cherry-pick <commit-id>
git rebase <branch>
git reflog
git bisect start
git archive --format=zip HEAD > repo.zip

## Cleanup & Maintenance
git gc
git fsck
git prune

## GitHub CLI (Optional)
gh auth login
gh repo create
gh repo clone <user/repo>
gh issue list
gh pr create
gh pr merge
gh pr checkout <id>

## Useful Aliases
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status

## Most Common Commands
git add .
git commit -m "message"
git push origin main
git pull origin main
