# electron-mattermost
Desktop app for [Mattermost](http://www.mattermost.org/) that runs on [Electron](http://electron.atom.io/)


## Features

### Desktop integration
* Badges for unread channels
* Notification
  * Windows 10: Toast
  * Windows 7-8.1: Balloon
  * OS X: Notification Center
  * Linux: libnotify ([Electron's notification spec](http://electron.atom.io/docs/v0.35.0/tutorial/desktop-environment-integration/#linux))
* Resident application

### Pre-packaged
You don't have to install any other software.


## Usage

### Installation
1. Download and unarchive a file from [release page](http://github.com/yuya-oc/electron-mattermost/releases).
2. Launch `electron-mattermost` in the unarchived folder.
3. After first launching, please input URL for your Mattermost team. For exmaple, `http://mattermost.example.com/team`.

### Quit
Ctrl or Command + Q to quit.

### Configuration
Configuration will be saved into Electron's userData directory:
* `%APPDATA%\electron-mattermost` on Windows
* `~/Library/Application Support/electron-mattermost` on OS X
* `~/.config/electron-mattermost` on Linux


## Testing
Node.js is required to test this app.

1. Clone or download the source code.
2. Run `npm install`.
3. Run `npm start`. (If you have gulp, `gulp serve` has live-reload.)


## Packaging
gulp is necessary for packaging this app.

```
$ npm install -g gulp (Or, use node_module/gulp/bin/gulp.js
```

You can package this app with following commands. Packages will be created in `release` directory.

```
$ gulp package (for your platform)
$ gulp package:windows (Requires Windows or Wine)
$ gulp package:osx (Requires OS X or Linux)
$ gulp package:linux
$ gulp package:all (Packages for all platform)
```
