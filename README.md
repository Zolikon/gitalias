# Git alias

 git config --global alias.lego 'log --oneline --decorate --graph -n 10'
 git config --global alias.save '!f() { git add . && git commit --amend --no-edit; }; f'
 git config --global alias.bname 'rev-parse --abbrev-ref HEAD'
 git config --global alias.down '!f() { git pull origin "$(git bname)"; };f'
 git config --global alias.up '!f() { git push origin $* "$(git bname)"; }; f'
 git config --global alias.comm '!f() { git add . && git commit -m "$(git bname) $*"; }; f'
 git config --global alias.commonBase 'merge-base master head'
 git config --global alias.changed '!f() { git diff --name-only "$(git commonBase)"; };f'
 git config --global alias.aliases '!f() { git config --global -l | grep alias; };f'
