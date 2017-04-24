# Notes & Settings Files
Centpanel Settings
My Sublime Settings


### Git global setup
```
git config --global user.name "Your Name"
git config --global user.email "Your@email.com"
```
### Create a new repository
```
git clone https://${{link}}/githubupgrade.git
cd githubupgrade
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```
### Existing folder SAME SERVER
```
cd existing_folder
git init
git remote add origin https://${{link}}/githubupgrade.git
git add .
git commit
git push -u origin master
```
### Existing Git repository SAME SERVER
```
cd existing_repo
git remote add origin  https://${{link}}/githubupgrade.git
git push -u origin --all
git push -u origin --tags
```
# Existing Git repository DIFFRENT SERVER
### Changing a remote's URL
```
git remote -v
//origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
//origin  git@github.com:USERNAME/REPOSITORY.git (push)

git remote set-url origin https://github.com/USERNAME/OTHERREPOSITORY.git
git remote -v

```

### Switching remote URLs from HTTPS to SSH
```
git remote -v
//origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
//origin  https://github.com/USERNAME/REPOSITORY.git (push)

git remote set-url origin git@github.com:USERNAME/OTHERREPOSITORY.git
git remote -v
# Verify new remote URL
origin  git@github.com:USERNAME/OTHERREPOSITORY.git (fetch)
origin  git@github.com:USERNAME/OTHERREPOSITORY.git (push)
```

### Troubleshooting
```
git remote set-url sofake https://github.com/octocat/Spoon-Knife
fatal: No such remote 'sofake'
```
