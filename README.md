# Mac Setup

- [System Update](#system-update)
- [System Preferences](#system-preferences)
- [Google Chrome](#google-chrome)
- [LastPass](#lastpass)
- [Fonts](#fonts)
- [iTerm2](#iterm2)
- [Homebrew](#homebrew)

## System Update

First thing you should always do is update your system so **Apple Icon > Software Update...**

## System Preferences

Some tweaks I like to do right away...  Do as you prefer with these.

In **Apple Icon > System Preferences**:

- Trackpad > Tap to click
- Keyboard > Key Repeat > Fast (all the way to the right)
- Keyboard > Delay Until Repeat > Short (all the way to the right)
- Keyboard > Text > Uncheck all options, especially _use smart quotes and dashes_
- Dock > Automatically hide and show the Dock and position on screen to Right
- Sharing > Change your computer name to something shorter and nicer... I used **vault72**

## Google Chrome

You need a good browser... [Google Chrome](//google.com/chrome) is my favorite.  Download the *.dmg* file, click to install and follow instructions.

Afterwards, I suggest signing  into chrome with your google account and syncing.

## LastPass

If you have it synced from your earlier google accounts, you can just log into it.  Otherwise, download it, install it and use it for your passwords.

## Fonts 

Because you will be working with fonts all day long, it's a good idea to download a font you like.  Because you will be writing code, you need a good mono-spaced font to work with.  Lately I have been happy with [inconsolata](https://fonts.google.com/specimen/Inconsolata?selection.family=Inconsolata).  I suggest downloading it, unzipping it and installing it.  After you unzip it you install it by doubleclicking on the .ttf files and  clicking install.

## iTerm2

You will spend a lot of time on the command-line... install a good one.  I suggest [iTerm2](https://www.iterm2.com/).  Download it, unpack it, then drag it into Applications.

Open iTerm2 by hitting **cmd+spacebar** and typing _iterm_.  Follow the instructions to give it full disk access.

Since you will be using iterm so much, let's make it prettier.

In **iTerm2 > Preferences** on the **General** tab, uncheck everything in the *Closing* section.

In the tab **Profiles**, create a new one with the "+" icon, and rename it to your first name for example. Then, select **Other Actions... > Set as Default**. Finally, under the section **Window**, change the size to something better, like **Columns: 125** and **Rows: 35**.

In the tab **Colors** choose a preset from the dropdown in the bottom right and adjust to  your liking. I usually take _solarized light_.  I just like the way it looks.

In the **Text** tab, click **Change Font** and select your favorite monospaced font such as _Inconsolata_ at 14pt.

In the **Terminal** tab, check **Unlimited scrollback**.  Also, because I don't like sounds, check **Silence bell**.

You will also need some dotfiles to do all the good stuff.  _.bash_profile_ is called first, then it calls in the rest.  To get you started, pull down the three I have here:


When done, hit the red "X" in the upper left (saving is automatic in OS X preference panes). Close the window and open a new one to see the size change.

##  Dotfiles

You will need some good dotfiles to finish up your iterm setup.  I have three great ones to get you started... just run the following in your terminal  to download a [.aliases](https://raw.githubusercontent.com/pop42/mac-setup/master/.aliases),[.bash_profile](https://raw.githubusercontent.com/pop42/mac-setup/master/.bash_profile), [.bash_prompt](https://raw.githubusercontent.com/pop42/mac-setup/master/.bash_prompt) 

Copy and paste this in your terminal:  

```
cd ~ && curl -O https://raw.githubusercontent.com/pop42/mac-setup/master/.aliases && curl -O https://raw.githubusercontent.com/pop42/mac-setup/master/.bash_profile && curl -O https://raw.githubusercontent.com/pop42/mac-setup/master/.bash_prompt
```

Close and reopen your terminal once again and marvel at its beauty!

## Homebrew

A great way to install and manage many of the utilities you will need.  Open iTerm2 by hitting **cmd+spacebar** and typing _iterm_.   Then type **xcode-select --install** and hit return.  This will install xcode which will is needed for everything else.

Now `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` to install homebrew.  You will have to  type in your password once, but after this, you really should not ever need to _sudo_ again to install items.


