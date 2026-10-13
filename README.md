# Browser extension to open GitHub file links in your IDE

[![CircleCI](https://circleci.com/gh/lmichelin/open-github-links-in-ide.svg?style=svg)](https://circleci.com/gh/lmichelin/open-github-links-in-ide)

This browser extension allows you to open files in your IDE directly from GitHub, assuming the repository you are working on is cloned on your computer. When a fragment of a file is displayed, your IDE opens the file and puts the cursor at the desired line.

👉 Google Chrome: https://chrome.google.com/webstore/detail/open-github-in-ide/bmifnnfmccmleigpaolofacllndmfned

👉 Firefox: https://addons.mozilla.org/firefox/addon/open-github-in-ide/

<p align="center">
	<img src="screenshots/readme.png" />
<p>

## Getting started

Once the extension is installed:

- Click on the extension icon to open the settings popup
- Set the local path where GitHub repositories are cloned on your computer
- Select the IDE you want to use to open GitHub links
- Reload GitHub and start using the extension

## Supported IDEs:

- Microsoft
  - VS Code
  - VS Code Insiders
- VSCodium
- JetBrains
  - IntelliJ IDEA <span style="color: #999;">(via Toolbox)</span>
  - CLion <span style="color: #999;">(via Toolbox)</span>
  - GoLand <span style="color: #999;">(via Toolbox)</span>
  - PhpStorm <span style="color: #999;">(via Toolbox)</span>
  - WebStorm <span style="color: #999;">(via Toolbox)</span>
  - Any JetBrains editor (using built-in web server)

WSL with the Ubuntu distribution is also supported on VS Code, VSCodium and VS Code Insiders for Windows.

For IntelliJ IDEA, WebStorm, PhpStorm, PyCharm, CLion, etc. please make sure you have installed the [JetBrains Toolbox App](https://www.jetbrains.com/toolbox-app/) first. It supports jetbrains://ide-name/... URLs.
 
You can also use the built-in web server of any JetBrains editor (IDEA, WebStorm, PhpStorm, WebStorm, ...) instead of the url handler. For that you need to install the PHP plugin. See [here](https://www.jetbrains.com/help/idea/php-built-in-web-server.html) for more information. The built-in web server must be started on port 63342.

> To disable JetBrains warning "_'file' API is requested. Do you trust unknown host?_", you can go to `File > Settings > Build, Execution, Deployment > Debugger` and Check the _Allow unsigned requests_ in the _Built-in Server_ section.

## New features & bugs

Need a feature? Want to report a bug? Feel free to open an issue or a pull request!

## Contributing

- Clone the project
- Run `yarn` to install the dependencies
- Run `yarn dev` to start the development server
- On Google Chrome:
  - Open [chrome://extensions/](chrome://extensions/)
  - Enable developer mode
  - Click on `Load unpacked`
  - Select the `dist/chrome` folder
- On Firefox:
  - Open [about:debugging#/runtime/this-firefox](about:debugging#/runtime/this-firefox)
  - Click on `Load Temporary Add-on`
  - Select the `dist/firefox/manifest.json` file
- The extension and the pages using it will be automatically reloaded when you modify the source code

## Changelog

### Version 2026.10.13

- Bug fixed: Support the latest scheme of JetBrains IDEs via Toolbox
- Grouping IDEs by vendor in settings
- New versioning scheme: using current date as a plugin version

### Version 1.2.3 - 2023-09-23

- Fix bug: icon was not showing in conversations after an update on GitHub side

### Version 1.2.2 - 2022-11-28

- Add support for CLion ([#39](https://github.com/lmichelin/open-github-links-in-ide/pull/39))

### Version 1.2.1 - 2011-08-18

- Add support for GoLand ([#32](https://github.com/lmichelin/open-github-links-in-ide/pull/32))

### Version 1.2.0 - 2022-08-11

- Add support for VS Code + WSL (Ubuntu) on Windows
- Migrate to manifest V3 on Chrome
- Fix bug: icon was not showing in file tree after an update on GitHub side
- Fix bug: icon was not showing in the "files changed" tab after clicking on it, a page reload was required ([#35](https://github.com/lmichelin/open-github-links-in-ide/issues/35))

### Version 1.1.14 - 2022-06-08

- Fix bug: icon was not showing in discussions after an update on GitHub side

### Version 1.1.13 - 2021-11-22

- Fix bug: extension was crashing on pull requests containing resolved conversations

### Version 1.1.12 - 2021-10-04

- Fix bug: icon was not showing on line numbers after an update on GitHub side

### Version 1.1.11 - 2021-04-18

- Add permission required on Firefox to use JetBrains built-in web server ([#20](https://github.com/lmichelin/open-github-links-in-ide/pull/20))

### Version 1.1.10 - 2021-04-05

- Fix an issue with JetBrains editors ([#17](https://github.com/lmichelin/open-github-links-in-ide/issues/17))

### Version 1.1.9 - 2021-03-20

- Update VSCodium icon

### Version 1.1.8 - 2021-03-14

- Fix bug: all line numbers were hidden when cursor was over a "Suggested changes" section in the "files changed" tab

### Version 1.1.7 - 2021-03-07

- Fix file header selector
- Show editor icon on file block lines in conversation tab
- Add support for JetBrains editors using built-in web server ([#16](https://github.com/lmichelin/open-github-links-in-ide/pull/16))

### Version 1.1.6 - 2020-09-27

- Add support for VSCodium ([#11](https://github.com/lmichelin/open-github-links-in-ide/pull/11))

### Version 1.1.5 - 2020-06-29

- Make extension compatible with new GitHub design

### Version 1.1.4 - 2019-10-23

- Add IntelliJ IDEA support

### Version 1.1.3 - 2019-07-21

- Add Firefox support 🎉
- Set the extension icon according to the selected IDE

### Version 1.1.2 - 2019-06-01

- Fix blurry icons on Retina screens

### Version 1.1.1 - 2019-06-20

- Use popup instead of options page

### Version 1.1.0 - 2019-06-16

- Show editor icon instead of line number when hovering over a line in file blocks
- Add options to select where to show the icon in GitHub
- Add option to show debug messages in console
- Fix some bugs

### Version 1.0.3 - 2019-06-15

- Add PhpStorm support

### Version 1.0.2 - 2019-06-14

- Add missing VS Code Insiders icon

### Version 1.0.1 - 2019-06-14

- Add VS Code Insiders support
- Add CSS theme for options page
- Open options page automatically after install

### Version 1.0.0 - 2019-06-06

- First release!
- Add VS Code support
