# Config

```
[user]
	name = Renan Henrique
	email = henriquebasshvf@gmail.com
[core]
	excludesfile = /Users/king/.gitignore_global
	editor = /usr/bin/vim
[difftool "sourcetree"]
	cmd = opendiff \"$LOCAL\" \"$REMOTE\"
	path = 
[mergetool "sourcetree"]
	cmd = /Applications/Sourcetree.app/Contents/Resources/opendiff-w.sh \"$LOCAL\" \"$REMOTE\" -ancestor \"$BASE\" -merge \"$MERGED\"
	trustExitCode = true
[commit]
	template = /Users/king/.stCommitMsg
[filter "lfs"]
	clean = git-lfs clean -- %f
	smudge = git-lfs smudge -- %f
	process = git-lfs filter-process
	required = true
[alias]
	g = git
  co = checkout
  cb = checkout -b
  st = status -sb
  sf = show --name-only
  fo = fetch origin
	r = rebase
	ri = rebase -i
	rc = rebase --continue
	ra = rebase --abort
	up = "!f() { git fetch origin && git remote prune origin && git checkout develop && git rebase origin/develop; }; f"
	nw = "!f() { git up && git checkout -b \"$*\" && git push --set-upstream origin \"$(git rev-parse --abbrev-ref HEAD)\" -f; }; f"
 	ci = "!f() { git commit -a -m \"$*\"; }; f"
  ck = "!f() { git checkout \"$*\" && git pull origin \"$*\" --rebase; }; f"
	po = "!f() { git push origin \"$(git rev-parse --abbrev-ref HEAD)\"; }; f"
	pf = "!f() { git push origin \"$(git rev-parse --abbrev-ref HEAD)\" -f; }; f"
	ub =  "!f() { git pull origin \"$*\" --rebase; }; f"
	rb = "!f() { git checkout master && git pull origin master --rebase && git rebase origin \"$(git rev-parse --abbrev-ref HEAD)\"; }; f"
  lg = log  --pretty=format:'%Cred%h%Creset %C(bold)%cr%Creset %Cgreen<%an>%Creset %s' --max-count=50
```
