# Mac Setup

- [System Update](#system-update)
- [System Preferences](#system-preferences)
- [Google Chrome](#google-chrome)
- [LastPass](#lastpass)
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

## Google Chrome

You need a good browser... [Google Chrome](//google.com/chrome) is my favorite.  Download the *.dmg* file, click to install and follow instructions.

Afterwards, I suggest signing  into chrome with your google account and syncing.

## LastPass

If you have it synced from your earlier google accounts, you can just log into it.  Otherwise, download it, install it and use it for your passwords.

## iTerm2

You will spend a lot of time on the command-line... install a good one.  I suggest [iTerm2](https://www.iterm2.com/).  Download it, unpack it, then drag it into Applications.

Open iTerm2 by hitting **cmd+spacebar** and typing _iterm_.  Follow the instructions to give it full disk access.

## Homebrew

A great way to install and manage many of the utilities you will need.  Open iTerm2 by hitting **cmd+spacebar** and typing _iterm_.   Then type **xcode-select --install** and hit return.  This will install xcode which will is needed for everything else.

Now `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` to install homebrew.
