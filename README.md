# Git Alias

## Summary
Essential goal of Git Alias is to turns Git command into shortest possible sequence of characters (an alias) where the alias value does not have to be remembered by the user but it  can be mnemotechnically derived from the non-shortened command.

- Full list of aliases is available [here](aliases.gitconfig).
- There is special alias `alias` that lists all aliases (alias for `config --global --get-regexp ^alias\\.`)

## Command Aliases

| Command| Alias |
| --- | --- |
| **`add`** | **`a`** |
| **`branch`** | **`b`** |
| **`commit`** | **`c`** |
| **`diff`** | **`d`** |
| **`rebase`** | **`e`** |
| **`fetch`** | **`f`** |
| **`log`** | **`g`** |
| **`stash`** | **`h`** |
| **`config`** | **`i`** |
| **`clone`** | **`k`** |
| **`pull`** | **`l`** |
| **`merge`** | **`m`** |
| **`clean`** | **`n`** |
| **`checkout`** | **`o`** |
| **`push`** | **`p`** |
| **`restore`** | **`r`** |
| **`switch`** | **`s`** |
| **`reset`** | **`t`** |
| **`status`** | **`u`** |
| **`revert`** | **`v`** |
| **`cherry-pick`** | **`y`** |

## Most Used Aliases

| Command | Alias |
| --- | --- |
| `add --all` | `aa` |
| `branch --all` | `ba` |
| `branch --delete --force` | `bdf` |
| `branch --move` | `bm` |
| `branch --remotes` | `br` |
| `commit --all` | `ca` |
| `commit --message` | `cm` |
| `diff --cached` | `dc` |
| `rebase main` | `em` |
| `fetch --all` | `fa` |
| `fetch --tags` | `ft` |
| `log --max-count` | `gmc` |
| `log --oneline` | `go` |
| `log --patch` | `gp` |
| `stash list` | `hl` |
| `stash pop` | `hp` |
| `pull --all` | `la` |
| `pull --rebase` | `lr` |
| `merge main` | `mm` |
| `merge --no-commit` | `mnc` |
| `merge --no-commit --squash` | `mncs` |
| `merge --squash` | `ms` |
| `clean --dry-run` | `ndr` |
| `clean --force` | `nf` |
| `clean --force --dry-run` | `nfdr` |
| `checkout` | `o` |
| `checkout -b` | `ob` |
| `push --force` | `pf` |
| `push --delete origin` | `pdo` |
| `push --set-upstream origin` | `psuo` |
| `push --tags` | `pt` |
| `restore --staged` | `rs` |
| `switch --create` | `sc` |
| `switch main` | `sm` |
| `reset --hard` | `th` |
| `reset --mixed` | `tm` |
| `revert --no-commit` | `vnc` |
| `cherry-pick` | `y` |
| `cherry-pick --no-commit` | `ync` |

## Rules

Each alias is created according to several predefined rules:

### 1) Each command is represented by a single letter
- `merge` turns into `m`

### 2) Each parameter/value is represented by combination of first letter of words it consists of
- `--no-commit` turns into `nc`
- `merge --no-commit --squash` turns into `mncs`
- Branch `main` is represented by letter `m`

#### Special Cases
- If the short parameter is uppercase letter then the letter is doubled
  - `checkout -B` turns into `obb`

### 3) Parameters are sorted in alphabetical order
- `merge --no-commit --squash` turns into `mncs`

#### Special Cases
- Parameter `--dry-run` is always the last one.
- When the alias contains parameter that requires value to be specified by the user, that parameter is the last one.
  - `log --oneline --max-count <MAX_COUNT>` turns into `lomc`
