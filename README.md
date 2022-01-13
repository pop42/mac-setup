# Mac Setup

## TOC

- [System Update](#system-update)
- [System Preferences](#system-preferences)
- [Google Chrome](#google-chrome)
- [LastPass](#lastpass)
- [Fonts](#fonts)
- [iTerm2](#iterm2)
- [Homebrew](#homebrew)
- [Git](#git)
- [VSCode](#vscode)
- [Node](#node)
- [awscli](#awscli)
- [Docker](#docker)
- [Slack](#slack)
- [Projects](#projects)

## System Update

First thing you should always do is update your system so **Apple Icon > Software Update...**

## System Preferences

Some tweaks I like to do right away... Do as you prefer with these.

In **Apple Icon > System Preferences**:

- Trackpad > Tap to click
- Keyboard > Key Repeat > Fast (all the way to the right)
- Keyboard > Delay Until Repeat > Short (all the way to the right)
- Keyboard > Text > Uncheck all options, especially _use smart quotes and dashes_
- Dock > Automatically hide and show the Dock and position on screen to Right
- Sharing > Change your computer name to something shorter and nicer... I used **vault72**

## Google Chrome

You need a good browser... [Google Chrome](//google.com/chrome) is my favorite. Download the _.dmg_ file, click to install and follow instructions.

Afterwards, I suggest sign in to chrome with your Google account and syncing.

## Passwords

Use Lastpass or 1Password. Either works.

If you have it synced from your earlier Google accounts, you can just log into it. Otherwise, download it, install it and use it for your passwords.

## Fonts

Because you will be working with fonts all day long, it's a good idea to download a font you like. Because you will be writing code, you need a good mono-spaced font to work with. Lately I have been happy with [inconsolata](https://fonts.google.com/specimen/Inconsolata?selection.family=Inconsolata). I suggest downloading it, unzipping it and installing it. After you unzip it you install it by doubleclicking on the .ttf files and clicking install.

## iTerm2

You will spend a lot of time on the command-line... install a good one. I suggest [iTerm2](https://www.iterm2.com/). Download it, unpack it, then drag it into Applications.

Open iTerm2 by hitting **cmd+spacebar** and typing _iterm_. Follow the instructions to give it full disk access.

Since you will be using iterm so much, let's make it prettier.

In **iTerm2 > Preferences** on the **General** tab, uncheck everything in the _Closing_ section.

In the tab **Profiles**, create a new one with the "+" icon, and rename it to your first name for example. Then, select **Other Actions... > Set as Default**. Finally, under the section **Window**, change the size to something better, like **Columns: 125** and **Rows: 35**.

In the tab **Colors** choose a preset from the dropdown in the bottom right and adjust to your liking. I usually take _solarized light_. I just like the way it looks.

In the **Text** tab, click **Change Font** and select your favorite monospaced font such as _Inconsolata_ at 14pt.

In the **Terminal** tab, check **Unlimited scrollback**. Also, because I don't like sounds, check **Silence bell**.

When done, hit the red "X" in the upper left (saving is automatic in OS X preference panes). Close the window and open a new one to see the size change.

## Oh My ZSH

Oh My ZSH makes your terminal experience just that much better... go ahead and download it. [zsh](https://ohmyz.sh/#install)

An aliases.zsh file will make your life a ton better.  Basically, it's shortcuts inside of your terminal.  For example, rather than having to type "cd .." you can just type .., or "dc up" instead of "docker-compose up"


Copy and paste this in your terminal:

    cd $ZSH_CUSTOM
curl -OOOO https://raw.githubusercontent.com/pop42/mac-setup/main/zsh_custom/\{aliases.zsh,exports.zsh,nvm.zsh,paths.zsh\}
    ls -la

Close and reopen your terminal once again and marvel at its beauty!

Whenever you find yourself typing the same commands over and over, feel free to edit that .profile file inside of $ZSH_CUSTOM!

## Homebrew

A great way to install and manage many of the utilities you will need. Open iTerm2 by hitting **cmd+spacebar** and typing _iterm_. Then type **xcode-select --install** and hit return. This will install xcode which will is needed for everything else.

Now `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` to install homebrew. You will have to type in your password once, but after this, you really should not ever need to _sudo_ again to install items.

# Git

Gotta have it.

`brew install git`

To allow bash-completion in git, `brew install bash-completion`

Now lets get it configured a bit.

`cd ~ && curl -O https://raw.githubusercontent.com/pop42/mac-setup/master/.gitconfig` will give you some nice colors for the status, branch and diff commands

also.. set your user info:

    git config --global user.name "Your Name Here"
    git config --global user.email "your_email@youremail.com"

And your osKeyChain so you don't have to keep typing your password over and over.

    git config --global credential.helper osxkeychain
    git config -l

## Webstorm/DataGrip

You need an editor to work in. Webstorm is pretty awesome and works for both macs and windows. Download it from [here](https://www.jetbrains.com/webstorm/download/#section=mac) unzip it, and drag it to the Applications directory.

DataGrip allows you to easily query and manage databases.  Download it from [here](https://www.jetbrains.com/datagrip/download/#section=mac)

# node

We will install node via _nvm_. To install nvm, go to [nvm install](https://github.com/creationix/nvm#install-script) and find the curl command to run. It looks something like `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash`

Then close your terminal, reopen it and type `command -v nvm` and if you see `nvm` as a response, you are good to go.

To install the latest node version, type `nvm install node`. To learn more about using nvm, go to [nvm](https://github.com/creationix/nvm)

Now install a few useful global modules we are currently using:

    npm i -g jest npm-check serverless

# awscli

If you are working directly with aws, you might need the awscli

    brew install awscli

# Docker

Download and install [docker for mac](https://store.docker.com/editions/community/docker-ce-desktop-mac). I believe they new ask you to login before downloading...


# Projects

I generally create a ~/projects directory and use it for most all the development work I do. Within that directory, I may create a /personal and a /work directory to separate my personal work from my actual work.

#Microsoft Remote Desktop

Go ahead and search for Remote Desktop in the app store and install that if you are on a mac!
