The first step is to install 'cowsay' and 'fortune'.  Fortune will give you the ability to get a random quote from the command line and cowsay will make the cow say the thing.  Lolcat will make it pretty. You can do this in OSX through the following commands

```bash
brew install cowsay
brew install fortune
gem install lolcat
```

To open your bash profile, use a text editor to open it with a command similar to the one below

```bash
atom ~/.bash_profile
```

Add the following alias to your bash profile
```bash
alias cow='fortune | cowsay | lolcat'
```

The following bash function will launch a new terminal and run the 'cow' alias. 
This will happen after 2500 seconds (45 minutes) after you type 'cowdoro' in the terminal.

```bash
function cowdoro {
  sleep 2500;
  osascript -e 'tell application "Terminal" to do script "cow"';
  osascript -e 'tell application "Terminal" to activate'
}```
