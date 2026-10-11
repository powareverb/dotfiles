# Notes

<https://www.chezmoi.io/quick-start/>

Update from remote source

```sh
# Update from remote source
chezmoi update
# Alias: chezup
```

Activate mise/starship with chezmoi (should auto activate in bashrc, but here as a backup)

```sh
source ~/.bash_profile
# Alias: refreshenv

# Activate mise
eval "$(mise activate)"
# Alias: activate-mise

# Activate starship
eval "$(starship init bash)"
# Alias: activate-starship
```

```sh
# Do some things
chezmoi add ~/.bashrc
chezmoi edit ~/.bashrc

chezmoi edit ~/.gitconfig

# See what is yet to change
chezmoi git status

# Add any untracked files
chezmoi git add .

# Something is different locally?
chezmoi diff
chezmoi status

# Shows differences in .bashrc
> diff --git a/.bashrc b/.bashrc

# Add the change to chez
chezmoi add ~/.bashrc

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
# Check upstream changes
chezmoi update

# Check incoming changes - manwelly
chezmoi git pull -- --autostash --rebase && chezmoi diff

# Check latest
chezmoi diff
chezmoi status
chezmoi -v apply
```
