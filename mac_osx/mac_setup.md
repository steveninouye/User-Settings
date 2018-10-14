# Mac OS X Setup

## Applications
- Google Chrome
- Visual Studio Code
- Atom
- Discord
- Slack
- WeChat
- WhatsApp

---
## Terminal Software
### Xcode
```
xcode-select --install
```
### Homebrew 
- Get Homebrew at [https://brew.sh](https://brew.sh/)
- After installing Homebrew install wget
```
 brew install wget
```
### Git
```
# install git
brew install git

# makes git terminal output pretty
git config --global color.ui true

# this will mark you as the 'author' of each committed change
git config --global user.name "your name here"

# use the email associated with your GitHub account
git config --global user.email your_email_here
```

#### Generating a new SSH key
![](ssh_key_gen.png)
![](new_ssh_agent.png)
![](add_gh_ssh_key.png)
### Fonts
```
# install fonts
brew tap caskroom/fonts
brew cask install font-fira-code
brew cask install font-inconsolata
```

---
## ~/.bash_profile
Create a `.bash_profile` in home directory and insert code inside.

*More Information to Customize Terminal Color at [Marina Mele's Site](http://www.marinamele.com/2014/05/customize-colors-of-your-terminal-in-mac-os-x.html)*
```
alias gac="git add -A && git commit -m "
alias gp="git push"
alias bsp="bundle exec rspec"
export CLICOLOR=1
export LSCOLORS=Gxheahdhfxegedabagacad
export HISTIGNORE="clear"
PS1="\e[3;37m\]💰 \d \A \h[\u]: \w 💰\n\e[0;37m\]💰 \e[0m\]"
HISTCONTROL=""
last_was_blank() { 
    local last_command="$(history 1)" 
    if [[ "$last_was_blank_PREVIOUS_LINE" != "$last_command" ]] ; 
    then
    echo ""
    fi 
    export last_was_blank_PREVIOUS_LINE="$last_command" 
    }
PROMPT_COMMAND=last_was_blank
```
Run `.bash_profile`.  In terminal run
```
source ~/.bash_profile
```


---
## Terminal 
```
# terminal default colors
BACKGROUND = black
TEXT = flora
BOLD TEXT = black # default
SELECTION = iron

# customize terminal color 
## terminal font
Monaco 12 pt

## terminal preferences
Display ANSI colors  # check the box
```