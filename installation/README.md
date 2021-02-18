# Guideline for Installaton and Tailoring of Operating System and Applications

Version: 2021-02-14

This is a checklist and guideline for anyone who is setting up a computer at the Centre.

A person who has perviously performed this installation and tailoring should provide guidance to anyone attempting this for the first time. 

The actions to perform that are listed below are abreviated and prior knowledge and experience is required in order to fully understand what to do.

## Installation

* Download latest Long Term Support (L.T.S.) distro from Ubuntu Mate [repository](https://ubuntu-mate.org/download/amd64/).

* Copy to a USB stick: See *Ubuntu/Ubuntu MATE* in https://ubuntu-mate.org/faq/usb-image/

* Boot the USB stick with a blank SSD as drive /dev/sda.

* Install Ubuntu from USB to SSD, with following parameters:
    - English Language
    - USA keyboard
    - Use entire SSD disk as one partition.
    - Account Administrator / administrator
    - Computer Name: *hp_1* or *dell_1*, *len_1*, etc.
    - Password: Use the default administrator password
    - Set password on login
    - Set Auckland Time zone

Upon completing remove the USB drive and reboot. The system should now come up from booting the SSD.


## Updating

* Log into Administrator account

* Turn off sending telemetry data and the login splash screen.

* Go on-line.

* Type `Ctrl Alt t` to open a terminal window.

* Add additional software packages by entering the commands:
```
$ sudo apt install gimp blender inkscape
$ sudo apt install gnome-games games-educaton
```

* Install patches to take to latest revision. `Ctrl Alt T` to open terminal window.
```    
$ sudo apt update
$ sudo apt dist-upgrade
```
* Reboot and then `$ sudo apt autoremove`.

## Tailoring Administrator account

* Menu --> Control Centre > MATE Tweak --> Panel. Select a panel layout to change the user interface. Select **Traditional** and then *Close* window. This provides a main menu with *Applications*, *Places* and *System*.

*  System --> Control Centre --> Screensaver.
    - Uncheck Activate screensaver when computer is idle.
    - Uncheck Lock screen when screensaver is active.
    - Close

*  System --> Control Centre --> Power Management.
    - *On AC Power* tab, set both options to *Never*.

* Launch Writer. Applications --> Office --> LibreOffice Writer. 
    - Select Tools --> Extension Manager. Click on *Get more extensions online...*. This opens a browser at https://extensions.libreoffice.org/.

    - In the *what are you looking for* enter *Zealand*. Click on *New Zealand Spellchecker*. Click on *Download*. Open with Libre Office (default)
    - Click OK to install.
    - Restart Writer.
    - Enter a Maori place name, like *Whanganui* and spell it incorrectly. See if the spellchecker will prompt with the correct spelling.

* Set preferences for Pluma. Applications --> Accessories --> Pluma. Edit --> Preferences --> Font and colors. 
    - Uncheck “Use the system fixed font width” 
    - Click on the Editor Font and increase size to 15. 
    - In the Color Scheme select *Colbalt*.

* Set preferences for Terminal. Applications --> System Tools --> MATE Terminal. Edit --> Profile Preferences. 
    - Uncheck *Use the system fixed width font* click on the *Font*. Increase size to “14”.
    - Click the Colors tab. Uncheck *Use colors from the system theme*. 
    - Click on the Scrolling tab and check *Unlimited*

* Set preferences for Mozilla Firefox.
    - General --> Startup. Check *Restore previous session*.

    - Language. Choose the languages used to display menus, messages, and notifications from Firefox.
    - Select *English (United Kingdom)* then restart.

    - Privacy and Security --> Firefox Data Collection and Use. Uncheck the following:
        - Allow Firefox to send technical and interaction data to Mozilla
        - Allow Firefox to make personalised extension recommendations
        - Allow Firefox to install and run studies
        - Allow Firefox to send backlogged crash reports on your behalf

* Workspaces. Right click Preferences. Set workspaces = 1

## Adding User Accounts

The User Accounts *Enderley* and *Career* are created.

* System --> Control Center --> Users and Groups.
    - Add *Enderley* Account
        - Click on Add. Enter Administrator password.
        - *New User Window* is displayed. Name: *Enderley* and accept Username: *enderley*. Click *OK*.
        - Click on *Change Users Password*. New Password: 12345678 Confirmation: 12345678
        - Check *Don’t ask for password on login*.
        - Click *OK*
        - Click on *Account type:* Click on *Change*.  Select *Desktop user*.

    - Add *Career* Account
        - Click on Add.
        - *New User Window* is displayed. Name: *Career* and accept Username: *career*. Click *OK*.
        - Click on *Change Users Password*. New Password: papanui Confirmation: papanui
        - Leave Unchecked *Don’t ask for password on login*.
        - Click *OK*
        - Click on *Account type:* Click on *Change*.  Select *Desktop user*.    
        - Close

## Computer system box

* Remove any Microsoft labels


