# Configs

```
export ZSH="/Users/king/.oh-my-zsh"

export GRAILS_OPTS="-server -Xmx4000M -XX:MaxPermSize=4000m"

# ZSH_THEME="refined"
ZSH_THEME="spaceship"

plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
)


export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

source $ZSH/oh-my-zsh.sh
source "$HOME/.sdkman/bin/sdkman-init.sh"

export JAVA_HOME="/Applications/Android Studio.app/Contents/jre/jdk/Contents/Home"

autoload -U promptinit; promptinit
export ANDROID_HOME=/Users/king/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
export DEFAULT_USER="$USER"

export PATH="$PATH:$HOME/.rvm/bin"
export PATH=/Users/king/development/flutter/bin:$PATH
export PATH=/Users/king/Documents/flutter/bin:$PATH

SPACESHIP_PROMPT_ORDER=(
  user          # Username section
  dir           # Current directory section
  host          # Hostname section
  git           # Git section (git_branch + git_status)
  hg            # Mercurial section (hg_branch  + hg_status)
  exec_time     # Execution time
  line_sep      # Line break
  vi_mode       # Vi-mode indicator
  jobs          # Background jobs indicator
  exit_code     # Exit code section
  char          # Prompt character
)
SPACESHIP_USER_SHOW=always
SPACESHIP_PROMPT_ADD_NEWLINE=true
SPACESHIP_CHAR_SYMBOL="👉 "
SPACESHIP_CHAR_SUFFIX=" "
#THIS MUST BE AT THE END OF THE FILE FOR SDKMAN TO WORK!!!
export SDKMAN_DIR="/Users/king/.sdkman"
[[ -s "/Users/king/.sdkman/bin/sdkman-init.sh" ]] && source "/Users/king/.sdkman/bin/sdkman-init.sh"

export PATH="$PATH:/path/to/elixir/bin"
```
