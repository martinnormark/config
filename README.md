# Config

**Config** is a basic checklist I follow to set up a new Mac's development environment. It gets me up to speed with Git, Ruby, GitHub, Jekyll, and more so I can more quickly get back to coding.

## Contents

| File | Description |
| --- | --- |
| `.bash-profile` | Customizes the Terminal.app prompt and echos the currently checked out Git branch. |
| `.gitconfig` | Global Git configuration to specify my name and email, shortcuts, colors, and more. |
| `.gitignore` | The ignore file from [twbs/bootstrap](https://github.com/twbs/bootstrap) that I use everywhere. |
| `Preferences.sublime-settings` | My Sublime Text 2 user preferences. |

## Checklist

### 1. Prep OS X

- Download and install latest version of Xcode from the Mac App Store
- Download and install Xcode command line tools

### 2. Download dependencies

- Install common gems: `$ gem install sass jekyll rouge`
- Download and run the [Node.js Mac installer](http://nodejs.org/download/)
- Install Grunt command line tools: `$ npm install -g grunt-cli`

### 3. Secure Git(Hub) access

- [Generate new SSH key](https://help.github.com/articles/generating-ssh-keys/)
- [Generate an access token](https://help.github.com/articles/creating-an-access-token-for-command-line-use/) for Terminal to auth your GitHub account when 2FA is enabled

### 4. Prep Terminal.app

- Load [`.bash_profile`](/.bash_profile)
- Load [`.gitconfig`](/.gitconfig) contents into the global `~/.gitconfig`
- Tweak color scheme

### 5. Setup Xcode + dependencies

- (Optional) [Import iOS/Mac developer profile](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/MaintainingCertificates/MaintainingCertificates.html#//apple_ref/doc/uid/TP40012582-CH31-SW15)
- If you didn't import, [add your Apple ID account to Xcode](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/ManagingAccounts/ManagingAccounts.html#//apple_ref/doc/uid/TP40012582-CH24-SW2)
- Install [Alcatraz](http://alcatraz.io/) `curl -fsSL https://raw.github.com/supermarin/Alcatraz/master/Scripts/install.sh | sh`
- Install [cocoapods](http://cocoapods.org/) `gem install cocoapods` (given permission errors, run the command elevated with `sudo`)
- Install [Dash for iOS](http://kapeli.com/dash_ios)
- Install [PaintCode](http://www.paintcodeapp.com/)
- Install [xScope](http://xscopeapp.com/)
- Install [Sip](https://itunes.apple.com/us/app/sip/id507257563?mt=12)
- Install [Tokens](http://usetokens.com/)

### 6. Tweak Sublime Text 2 just right

*I use Sublime Text 2 as ST3 had quite a few problems the first day I used it with Yosemite. You'll need to modify your approach below if you're using ST3.*

- [Install Package Control](https://sublime.wbond.net/installation):
  - Open Sublime Text 2 and hit `Ctrl-\``, then enter the following:
```bash
import urllib2,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```
- Install and load packages (`Cmd-Shift-P`):
  - [Spacegray theme](http://kkga.github.io/spacegray/) 
  - [Sass](http://sass-lang.com) package
- Load user settings from [`Preferences.sublime-settings`](/Preferences.sublime-settings)

### 7. Download Atom

- Install Atom itself
- Add Spacegray UI theme and Ocean Dark color scheme
- Enable `atom` Terminal commands: from Atom.app, open the Atom menu and select *Install Shell Commands*

## Use it yourself

Fork this repo, or just copy-paste things you need, and make it your own. **Please be sure to change your `.gitconfig` name and email address though!**

## Works on my machine

Yup, it does. Hopefully it does on yours as well, but please don't hate me if it doesn't.

<3
