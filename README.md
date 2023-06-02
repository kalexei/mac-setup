## My Mac Setup

This repo contains info on all the apps / tools / settings I use on my Mac.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [What Macbook do I have?](#what-macbook-do-i-have)
- [Homebrew / Terminal / Shell](#homebrew--terminal--shell)
  - [Homebrew](#homebrew)
  - [Terminal](#terminal)
  - [Shell](#shell)
    - [Install Bash and set it as the default](#install-bash-and-set-it-as-the-default)
    - [Customizing Bash with `.bash_profile`](#customizing-bash-with-bash_profile)
    - [Commands used by my .bash_profile](#commands-used-by-my-bash_profile)
    - [Install the latest version of git](#install-the-latest-version-of-git)
    - [Other command line tools I use](#other-command-line-tools-i-use)
- [OS Productivity](#os-productivity)
  - [Window Management](#window-management)
  - [App Switching](#app-switching)
  - [Quick Launching](#quick-launching)
- [Other Apps I Use Daily](#other-apps-i-use-daily)
- [OS Settings](#os-settings)
  - [Finder](#finder)
  - [Dock](#dock)
- [Menu Bar Customization](#menu-bar-customization)
  - [System Stats Widgets](#system-stats-widgets)
  - [Menu Bar Calendar](#menu-bar-calendar)
- [Note Taking](#note-taking)
- [Web Browser](#web-browser)
  - [Firefox](#firefox)
- [Node.js](#nodejs)
  - [Global Modules](#global-modules)
- [VS Code](#vs-code)
- [Break Timer](#break-timer)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## What Macbook do I have?

I am using the 2020 M1 13" Macbook Pro.

Specs:
* Apple M1 Pro
* 16GB RAM
* 256GB SSD

## Homebrew / Terminal / Shell

### Homebrew

[Homebrew](https://brew.sh/) lets you install tools and apps from the command line.

### Terminal

I prefer [iTerm2](https://iterm2.com/)

```
brew install iterm2
```

* Appearance
  * Theme
    * Minimal
* Profiles
  * Default
      * General -> Working Directory -> Reuse previous session's directory
      * Colors -> Basic Colors -> Foreground -> Lime Green
      * Text -> Font -> Anonymous Pro
          * You can download this font [here](https://www.marksimonson.com/fonts/view/anonymous-pro)
      * Text -> Font Size -> 36
      * Keys -> Key Mappings -> Presets -> Natural Text Editing

### Shell

Mac uses zsh by default, that's what I use

[Oh My Zsh](https://ohmyz.sh/) to customize zsh

#### Install the latest version of git

You can use brew to install the latest version of `git`:

```sh
brew install git
```

Configure git with your name / email and preferred editor:

```sh
git config --global user.name "YOURUSERNAME"

git config --global user.email "YOUREMAIL"
```

## OS Productivity

### Window Management

I use [rectangle](https://rectangleapp.com/) to move and resize windows using keyboard shortcuts.

```sh
brew install rectangle
```

### App Switching

[AltTab](https://alt-tab-macos.netlify.app/)

I replace the built-in `CMD+TAB` shortcut with AltTab.

```sh
brew install alt-tab
```

### Quick Launching

[Alfred](https://www.alfredapp.com/)

```sh
brew install alfred
```

## Other Apps

* [firefox-developer-edition](https://www.mozilla.org/en-US/firefox/developer/) - Web browser for development
* [app-cleaner](https://freemacsoft.net/appcleaner/)
* [vlc](https://www.videolan.org/)
* [keka](https://www.keka.io/en/) - Can extract 7z / rar and other types of archives
* [kap](https://getkap.co/) - Screen recorder / gif maker
* [time-out](https://www.dejal.com/timeout/) - Break timer
* [gimp](https://www.gimp.org/)
* [inkscape](https://inkscape.org/)
* [visual-studio-code](https://code.visualstudio.com/)
* [insomnia](https://insomnia.rest/products/insomnia) - HTTP / REST / GraphQL tester / requester

You can install them in one go by placing them all into a text file and then running brew install:

```
firefox-developer-edition
app-cleaner
vlc
keka
kap
time-out
gimp
inkscape
visual-studio-code
insomnia
```

```sh
xargs brew install < apps.txt
```

## OS Settings

These are my preferred settings for `Finder` and the `Dock`.

### Finder

* Finder -> Preferences
  * General -> Show these on the desktop -> Select None
      * I try to keep my desktop completely clean.
  * General -> New Finder windows show -> Home Folder
      * I prefer to see my home folder in each new finder window instead of recent documents
  * Advanced -> Show all filename extensions -> Yes
  * Advanced -> When performing a search -> Search the current folder
* View
  * Show Status Bar
  * Show Path Bar

### Dock

* System Preferences
  * Dock & Menu Bar
      * Size -> Small as possible
      * Position on screen -> Right
      * Automatically hide and show the Dock -> Yes

## Menu Bar Customization

### System Stats Widgets

[stats](https://github.com/exelban/stats)

Under "widget settings", choose "merge widgets into one".

```sh
brew install stats
```

## Web Browser

### Firefox

* Adblocker - [uBlock Origin](https://github.com/gorhill/uBlock)
* Tracker Blocker - [Privacy Badger](https://privacybadger.org/)
  * Firefox now includes tracker blocking, but I leave Privacy Badger enabled.
* [Cookie Autodelete](https://github.com/Cookie-AutoDelete/Cookie-AutoDelete)
  * Removes cookies from websites that are not in my whitelist whenever a tab is closed. An additional precaution to tracker blocking.
* [Decentraleyes](https://decentraleyes.org/)
  * Caches CDN links locally and intercepts requests to serve from the cache. Prevents CDNs from tracking you across websites.


## Node.js

See installation instructions [here](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
brew install nvm
```

### Global Modules

* lite-server
  * Auto refreshing static file server. Great for working on static apps with no build tools.
* license
  * Auto generate open source license files
* gitignore
  * Auto generate `.gitignore` files base on the current project type

```
npm install -g lite-server license gitignore
```

## VS Code

VS Code is my preferred code editor.

My settings / extensions [here](https://gist.github.com/kalexei/4007776a7aa2675346b2ac8e5549505c).

2 of the most notable settings are:

```json
{
  "editor.linkedEditing": true,
  "editor.snippetSuggestions": "top",
}
```
