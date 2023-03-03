# Config

```
[user]
	name = Renan O Henrique
	email = henriquebasshvf@gmail.com

[core]
	editor = code --wait

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
	lg1 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
	lg2 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all
	lg = !"git lg1" --max-count=50
  # lg = log  --pretty=format:'%Cred%h%Creset %C(bold)%cr%Creset %Cgreen<%an>%Creset %s' --max-count=50
```
