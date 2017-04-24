# Notes & Settings Files
Centpanel Settings
My Sublime Settings


# Git global setup
```
git config --global user.name "Jeeten P@tel"
git config --global user.email "jeeteshnariya@gmail.com"
```
# Create a new repository
```
git clone https://${{link}}/githubupgrade.git
cd githubupgrade
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```
# Existing folder
```
cd existing_folder
git init
git remote add origin https://${{link}}/githubupgrade.git
git add .
git commit
git push -u origin master
```
# Existing Git repository
```
cd existing_repo
git remote add origin  https://${{link}}/githubupgrade.git
git push -u origin --all
git push -u origin --tags
```
