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

The following bash function will launch a new terminal and run the 'cow' alias and push it in front of all of your windows. This will happen 2500 seconds (45 minutes) after you type 'cowdoro' in the terminal.

Add the following to your bash profile to enable this part. 

```bash
function cowdoro {
  sleep 2500;
  osascript -e 'tell application "Terminal" to do script "cow"';
  osascript -e 'tell application "Terminal" to activate'
}
```

When it runs, it should look something like this:

<img width="278" alt="screen shot 2017-07-28 at 10 44 13 pm" src="https://user-images.githubusercontent.com/20469703/28742167-55921218-73e6-11e7-975f-9bf1165c49de.png">

If you would prefer a penguin, you can add the -f tux flag to the cowsay command.  The penguin looks like this:

<img width="323" alt="screen shot 2017-07-29 at 11 02 16 am" src="https://user-images.githubusercontent.com/20469703/28746677-7cd4618e-744d-11e7-93fd-c21dbeacd45b.png">

