# Updating your system and installing and using applications

The following instructions are for macOS Catalina. If you are not on Catalina
but can upgrade, we recommend doing so _after_ following the instructions below.
Additional instructions are included in the steps below for non-Catalina users. 

You can check your OS version by clicking the apple menu in the top left and
clicking 'About This Mac'.

## Check that your macOS system is compatible with Flatiron School’s requirements

When working on software, it is important that your computer and the software that you’re using are compatible with each other. In this step, we’ll ensure that you are able to install all the tools that you will need to complete the program.

### Action item: check your macOS system specifications

1. Click on the Apple () menu in the top left of the window
2. Choose "About This Mac" from the menu
3. Look for the version name (for example, "macOS Catalina")
4. Look for the version number (for example, "Version 10.15.6")

### Check your work

If your version name is macOS Catalina and your version number is greater than "Version 10.15.0", your computer meets our requirements for the course and you can continue below. 

If your computer does not meet the requirements listed above, but you can upgrade, we recommend that you upgrade after completing the environment setup.

If your computer does not meet the requirements and you can't upgrade, some programs may not work for you. Please reach out to an instructor for more information.

## Check that your macOS system has enough space for Flatiron School’s requirements

The programs that we’ll be installing during environment setup plus all of the work that you’ll do with Flatiron School will need at least 4 GB of free disk space. Follow the steps below to ensure that you have enough disk space to install all the programs needed during environment setup.

<!-- TODO: Verify disk space needs; seems low -->

### Action item: Check your storage

1. Click on the Apple () menu in the top left of the window
2. Choose "About This Mac" from the menu
3. Click the "Storage" tab header
4. Look for your macOS partition (for example, "Macintosh HD")
5. Look for the storage (for example, "119.59 GB available of 186 GB")

### Check your work

If your free space for your macOS partition is greater than 4 GB, continue below. Otherwise, click "Manage..." to open the System Information window and free up some storage space.

## Install Command Line Tools for Xcode

Command Line Tools for Xcode is a suite of development tools from Apple, including tools for building Mac and iPhone applications. It will help you to quickly set up your environment by downloading and installing essential tools for other programs we'll be installing.

### Action item

1. Open the Apple Developer Download webpage (https://developer.apple.com/download/more/?=command%20line%20tools%20for%20xcode%2012)
2. Look for a description of "Command Line Tools for XCode 12"
3. Look for a release date of September 17, 2020
4. Click the "+" symbol to see more information about the download
5. Click "Command Line Tools for XCode 12.dmg" to download
6. When the download is finished, click on the file to install

### Check your work

Open the "Terminal" application using "Spotlight Search", type `xcode-select --install` and press `<Enter>`. If your terminal says "xcode-select: error: command line tools are already installed...", continue below.

## Install Homebrew

Homebrew is a package manager for macOS. It allows us to easily install a number of programs we will need. 

### Action item

1. Open the "Terminal" application using "Spotlight Search"
2. Type `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"` and press `<Enter>`
3. Follow the prompts on the screen during the installation (Note: this could take a while.)
4. Close the "Terminal" application
5. Reopen the "Terminal" application using "Spotlight Search"

### Check your work

You can verify that Homebrew is successfully installed by running `brew help`. If your terminal outputs a list of `brew` commands, you're all set.

<!-- HERE -->

## Install Zsh

Zsh is the new standard shell for the macOS and comes pre-installed with the latest version of macOS.

### Action item

1. Open the "Terminal" application using "Spotlight Search"
2. Type `echo $SHELL` and press `<Enter>`
3. Type `brew install zsh` and press `<Enter>`
4. Type `echo /usr/local/bin/zsh | sudo tee -a /etc/shells` and press `<Enter>` (Note: you will need to enter your password.)
5. Type `chsh -s /usr/local/bin/zsh` and press `<Enter>`
6. Close the "Terminal" application
7. Reopen the "Terminal" application using "Spotlight Search"

### Check your work

If you rerun `echo $SHELL`, the terminal should output `/usr/local/bin/zsh`, continue below.


## Install Google Chrome

Google Chrome is the browser that we will use for your Flatiron School Student Portal account and also for front-end web development. You are not required to use Google Chrome for personal work, but we highly encourage that you download it for access to your account and for development in the browser.

### Action item: download and install Google Chrome

1. Open the Google Chrome download webpage (https://www.google.com/chrome)
2. Click "Download Chrome" and "Accept and Install"
3. Wait for the "googlechrome.dmg" file to download and find it in the "Finder" application
4. Open the "googlechrome.dmg" file and install Google Chrome
5. Drag the "Google Chrome" application to your "Applications" folder

### Check your work

If you are able to open the "Google Chrome" application using "Spotlight Search", continue below.


## Install Visual Studio Code (VS Code) on Windows

Visual Studio Code (VS Code) is the tool that you’ll use to edit your Ruby and JavaScript files. It is a text editor that provides some really useful extensions for developers. One such tool is an integrated terminal! This means that you can edit your code and use your terminal in the same window. Follow the steps below to get both set up.

### Action item: download and install Visual Studio Code

1. Open the Visual Studio Code download webpage (https://code.visualstudio.com/Download)
2. Click on the Mac download option and start the download
3. Wait for the ".zip" file to download and find it in the "Finder" application
4. Open the ".zip" file and install Visual Studio Code
5. Drag the "Visual Studio Code" application to your "Applications" folder
6. Open the "Visual Studio Code" application using "Spotlight Search"
7. Click “View” in the toolbar, then click "Command Palette" in the dropdown menu, or use the shortcut <Command ⌘> + <Shift> + P
8. Type ">shell command" in the box and click on "Shell Command: Install 'code' command in PATH"
9. Close the "Visual Studio Code" application
10. Open the "Terminal" application using "Spotlight Search"
11. Type `code` and press `<Enter>`

### Check your work

If Visual Studio Code (VS Code) opened after typing `code` in your "Terminal" application, continue below.


<!-- I don't believe this is necessary... -->
<!-- If you would like to use the terminal built into VS Code, you may need to update
the settings. If you intend to use your regular terminal, you do not need to
complete this step.

To update VS Code's terminal settings, while in VS Code, press
`command(⌘) + shift(⇧) + p` and search for `settings.json`.

![VS Code settings.json](https://curriculum-content.s3.amazonaws.com/onboarding/vs%20code%20settings.png)

In this file, you should see opening and closing curly braces `{}` without
anything inside them. Add the following in between the braces:

```js
"terminal.integrated.env.osx": {
    "PATH": ""
}
```

If there are already items inside the curly braces, instead of erasing them, you
can add a comma after the last item and paste in the above setting on a new
line. The file should look like this:

```js
{
  "terminal.integrated.env.osx": {
    "PATH": ""
  }
}
```

Or something similar to this:

```js
{
  "some.other.settings.present": true,
  "do.not.forget.the.end.comma": true,
  "terminal.integrated.env.osx": {
    "PATH": ""
  }
}
``` -->


## Install Slack

### Action item

<!-- 1. Open the Slack download webpage (https://slack.com/download/mac)
2. Click on the Mac download option -->


### Check your work

<!-- Install Slack for Mac and enable desktop notifications for Slack. One week
before your start date, you will receive an invitation to join the Flatiron
School workspace, `flatiron-school.slack.com`. You’ll also receive a welcome
email with information about channels you should join. -->
