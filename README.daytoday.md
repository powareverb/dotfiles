# Notes

<https://www.chezmoi.io/quick-start/>

```sh
# Update from remote source
chezmoi update
```

```sh
chezmoi add ~/.bashrc
chezmoi edit ~/.bashrc

chezmoi edit ~/.gitconfig

# See what is yet to change
chezmoi git status

# Add any untracked files
chezmoi git add .

# Once happy, commit changes

# Using chezmoi wrappers
chezmoi git status
chezmoi git commit -m "Your commit message"
chezmoi git push

# If manual is needed
chezmoi cd
git status
git remote add origin https://github.com/$GITHUB_USERNAME/dotfiles.git
git config --global user.email "powareverb@gmail.com"
git config --global user.name "Gavin Jones"
git commit -m "Your commit message"
git push -u origin main
exit

```

```sh
# Check incoming changes
chezmoi git pull -- --autostash --rebase && chezmoi diff

# Check latest
chezmoi diff
chezmoi status
chezmoi -v apply
```
