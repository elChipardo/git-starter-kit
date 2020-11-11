# git starter kit

Want to save time using git? This is where your journey begins!

## Save your git credentials

**WARNING**: credentials are stored in plaintext.

### Globally

Credentials will be red from your home directory and will be stored in `~/.git-credentials` file.

```sh
$ git config --global credential.helper store
```

### Locally

Credentials will be red only from your repository and will be stored in `path/to/your/repository/.git-credentials` file.

```sh
$ git config credential.helper store
```

Then perform `git pull`, enter your credentials once and that's it, they are saved!

## Useful aliases

Add the following aliases into your initalization shell session file. It will depends on what shell you are using. It can be `.bashrc` or `.zshrc` and so on.

```bash
alias g='git'
alias ga='git add'
alias gaa='git add --all'
alias gbr='git branch'
alias gch='git checkout'
alias gchb='git checkout -b'
alias gc='git commit -m'
alias gd='git diff'
alias gf='git fetch'
alias yolo='git push --force'
alias grbi='git rebase -i'
alias grba='git rebase --abort'
alias grbc='git rebase --continue'
alias gst='git status'
alias gdlbr='git remote prune origin ; git branch -vv | grep '"'"': gone]'"'"'|  grep -v "\*" | awk '"'"'{print$1}'"'"' | xargs -r git branch -D' #gdlbr for git delete local branches
```

## Further details

[official git documentation](https://git-scm.com/docs/).
