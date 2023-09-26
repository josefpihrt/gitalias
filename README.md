# Gitalias <img align="left" width="48px" height="48px" src="images/gitalias-logo-small.png">

## Summary

Essential goal of Gitalias is to turns [git](https://git-scm.com/) command into shortest possible sequence of characters (an alias) where the alias does not have to be remembered but it can be mnemotechnically derived from the full command.

## Documentation

https://josefpihrt.github.io/docs/gitalias

## Usage

- Copy [list of aliases](https://raw.githubusercontent.com/JosefPihrt/gitalias/main/alias.gitconfig) and paste it to your [.gitconfig](https://git-scm.com/docs/git-config) file.

### Usage Example

#### Implement feature on a new branch
```sh
git th                 # reset --hard
git sm                 # switch main
git l                  # pull
git sc feature/foo     # switch --create feature/foo
                       # Implement feature ...
git aa                 # add --all
git cm "Implement foo" # commit --message "Implement foo"
```

#### Create and Merge PR

Use GitHub CLI or web UI ...

#### Clean feature branch
```sh
git sm              # switch main
git l               # pull
git opo             # remote prune origin
git bdf feature/foo # branch --delete --force feature/foo
```
