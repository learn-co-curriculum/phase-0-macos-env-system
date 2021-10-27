# MacOS System Setup

The following instructions are for macOS Catalina through BigSur. If you are not
on Catalina or a later operating system like BigSur but have the option to
update, we recommend doing so before following the instructions below.

**Note**: Throughout the environment setup, you will see commands that look like
this:

```console
$ whoami
```

Any time you see a command like this with a `$` at the beginning, those commands
should be entered in your terminal **without** the `$`. So for the example
above, you would type `whoami` in the terminal (without a `$`).

## Check That Your macOS System is Compatible with Flatiron School's Requirements

When working on software, it is important that your computer and the software
you're using are compatible. In this step, we'll ensure that you can install all
the tools you will need to complete the program.

### Action Item

1. Click on the Apple () menu in the top left of the window
2. Choose "About This Mac" from the menu
3. Look for the version name (for example, "macOS Big Sur")
4. Look for the version number (for example, "Version 11.4")

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/CF82Etkyfm8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>

If your version name is macOS Catalina, Big Sur, or Monterey, and your version
number is greater than "Version 10.15.0", your computer meets our requirements
for the course and you can continue below.

If your computer does not meet the requirements listed above, but you can
upgrade, we recommend that you upgrade after completing the environment setup.

If your computer does not meet the requirements and you can't upgrade, some
programs may not work for you. Please reach out to an instructor for more
information.

## Check that Your macOS System Has Enough Space for Flatiron School's Requirements

The programs that we'll be installing during environment setup and all of the
work you'll do with Flatiron School will need at least 4 GB of free disk
space. Follow the steps below to ensure that you have enough disk space to
install all the programs needed during environment setup.

### Action Item

1. Click on the Apple () menu in the top left of the window
2. Choose "About This Mac" from the menu
3. Click the "Storage" tab header
4. Look for your macOS partition (for example, "Macintosh HD")
5. Look for the storage (for example, "119.59 GB available of 186 GB")

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/0Z0BzmiTqsk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>

If your free space for your macOS partition is greater than 4 GB, continue
below. Otherwise, click "Manage..." to open the System Information window and
free up some storage space.

## Install Homebrew

[Homebrew][brew] is a package manager for macOS. It allows us to quickly install
a number of programs we will need.

[brew]: https://brew.sh

### Action Item

1. Open the "Terminal" application using "Spotlight Search"
2. Type `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"` and press `<Enter>`
3. Follow the prompts on the screen during the installation (Note: this could
   take a while.)
4. After the installation has completed, you may be prompted to run two
   additional commands to add Homebrew to your PATH. If so, run those two
   commands in your terminal.
5. Close the "Terminal" application
6. Reopen the "Terminal" application using "Spotlight Search"

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/igtyCPu3JNk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>

You can verify that Homebrew is successfully installed by running `brew help`.
If your terminal outputs a list of `brew` commands, you're all set.

## Check Whether You Need to Install Zsh

Zsh is the new standard shell for the macOS and comes pre-installed with the
latest version of macOS, but it may need to be installed on older Macs.

### Action Item

1. Open the "Terminal" application using "Spotlight Search"
2. Type `echo $SHELL` and press `<Enter>`
3. **If you see `/bin/zsh` or `/usr/local/bin/zsh` DO NOT continue with the next
   steps. Move on to "Check Your Work".**

Otherwise, to install Zsh:

1. Type `brew install zsh` and press `<Enter>`
2. Type `echo /usr/local/bin/zsh | sudo tee -a /etc/shells` and press `<Enter>`
   (Note: you will need to enter your password.)
3. Type `chsh -s /usr/local/bin/zsh` and press `<Enter>`
4. Close the "Terminal" application
5. Reopen the "Terminal" application using "Spotlight Search"
6. If you receive a message starting with "This is the Z Shell configuration
   function for new users, zsh-newuser-install", press `0`.

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/wiqcFoV2heU" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

If you run `echo $SHELL`, the terminal should output `/bin/zsh` or `/usr/local/bin/zsh`.
This indicates that Zsh is in use and you are set to continue below.

## Troubleshooting

If you see the following message when opening your terminal:

```console
zsh compinit: insecure directories, run compaudit for list.
Ignore insecure directories and continue [y] or abort compinit [n]?
```

Type `y` and press enter, then run the following command:

```console
$ compaudit | xargs chmod g-w
```

Close and reopen your terminal to clear the error.

## Install Google Chrome

Google Chrome is the browser that we will use for your Flatiron School Student
Portal account and also for front-end web development. You are not required to
use Google Chrome for personal work, but we highly encourage you to download it
for access to your account and for development in the browser.

### Action Item

1. Open the [Google Chrome download webpage][] (https://www.google.com/chrome)
2. Click "Download Chrome" and "Accept and Install"
3. Wait for the "googlechrome.dmg" file to download and find it in the "Finder"
   application
4. Open the "googlechrome.dmg" file and install Google Chrome
5. Drag the "Google Chrome" application to your "Applications" folder

[google chrome download webpage]: https://www.google.com/chrome

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/YS_qinEgacI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

If you can open the "Google Chrome" application using "Spotlight
Search", continue below.

## Install Visual Studio Code (VS Code)

Visual Studio Code (VS Code) is the tool that you'll use to edit your Ruby and
JavaScript files. It is a text editor that provides some beneficial extensions
for developers. One such tool is an integrated terminal! This means that you can
edit your code and use your terminal in the same window. Follow the steps below
to get both set up.

### Action Item

1. Open the [Visual Studio Code download webpage][]
   (https://code.visualstudio.com/Download)
2. Click on the Mac download option and start the download
3. Wait for the ".zip" file to download and find it in the "Finder" application
4. Open the ".zip" file and install Visual Studio Code
5. Drag the "Visual Studio Code" application to your "Applications" folder
6. Open the "Visual Studio Code" application using "Spotlight Search"
7. Click "View" in the toolbar, then click "Command Palette" in the dropdown
   menu, or use the shortcut `<Command ⌘> + <Shift> + P`
8. Type "shell command" in the box and click on "Shell Command: Install 'code'
   command in PATH"
9. Close the "Visual Studio Code" application
10. Open the "Terminal" application using "Spotlight Search"
11. Type `code` and press `<Enter>`

[visual studio code download webpage]: https://code.visualstudio.com/Download

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/5E2frsEGepE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

If Visual Studio Code (VS Code) opened after typing `code` in your "Terminal"
application, continue to the next lesson, **Installing Node on macOS**.
