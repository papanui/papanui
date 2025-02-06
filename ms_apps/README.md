# Microsoft Online Applications

Shorcuts for Microsoft Online Applications is a non-official version by Dejan Petrovic. It's current version is 1.0.
This provides launchers in:

* Applications --> Microsoft Online Apps
* Applications --> Office.

The product available to launch are:

* Calendar
* Excel
* OneDrive
* OneNote
* Outlook
* People
* PowerPoint
* Word

The package is: `microsoft_online_apps.deb`
It is downloaded from: `http://sourceforge.net/projects/microsoftonlineapps/files/v1.0.0/microsoft_online_apps.deb/download`

A tree of the expanded .deb file...
```
ian@hp:~/Enderley$ tree ms-online-apps/
ms-online-apps/
├── DEBIAN
│   └── control
├── etc
│   └── xdg
│       └── menus
│           └── applications-merged
│               └── microsoft.menu
└── usr
    └── share
        ├── applications
        │   ├── calendar.desktop
        │   ├── excel.desktop
        │   ├── onedrive.desktop
        │   ├── onenote.desktop
        │   ├── outlook.desktop
        │   ├── people.desktop
        │   ├── powerpiont.desktop
        │   └── word.desktop
        ├── desktop-directories
        │   └── microsoftonlineapps.directory
        └── icons
            └── microsoftonline
                ├── 0_calendar.png
                ├── 0_excelonline.png
                ├── 0_onedrive.png
                ├── 0_onenoteonline.png
                ├── 0_outlook.png
                ├── 0_people.png
                ├── 0_powerpointonline.png
                ├── 0_wordonline.png
                └── microsoftonlineapps.png
```

On 6 Feb 2025 Ian modified the package and created V2.0: Modifications are:

* No longer put launchers in `Application --> Office`
* Reduce apps to only launch:
* Excel
* OneDrive
* PowerPoint
* Word

The repackaging was done as follows:

* Downloaded `microsoft_online_apps.deb`
* Used `Engrampa Archive Manager` to expand all files from .deb package to the folder: `ms-online-apps`
* Removed 4 x .desktop files
* Updated the version number and description in `control` file
* From each *.desktop file removed the `Office` from the line: `Categories=Microsoft Online Apps;Office;`
* Fixed a typo bug with powerpoint.desktop` naming.
* Removed from `powerpoint.desktop` the line: `Name[en_GB]=powerpiont.desktop`
* Rebuilt the deb file with command: `dpkg-deb -b ms-online-apps microsoft-online-apps.deb`
* Installed the package using `GDebi Package Installer`

The V2.0 tree is:
```
ian@hp:~/Enderley$ tree ms-online-apps
ms-online-apps
├── DEBIAN
│   └── control
├── etc
│   └── xdg
│       └── menus
│           └── applications-merged
│               └── microsoft.menu
└── usr
    └── share
        ├── applications
        │   ├── excel.desktop
        │   ├── onedrive.desktop
        │   ├── powerpoint.desktop
        │   └── word.desktop
        ├── desktop-directories
        │   └── microsoftonlineapps.directory
        └── icons
            └── microsoftonline
                ├── 0_calendar.png
                ├── 0_excelonline.png
                ├── 0_onedrive.png
                ├── 0_onenoteonline.png
                ├── 0_outlook.png
                ├── 0_people.png
                ├── 0_powerpointonline.png
                ├── 0_wordonline.png
                └── microsoftonlineapps.png
```

The V2.0 `microsoft-online-apps.deb` file is in this papanui repository in the [ms_apps](./) folder.

Click to get to the github page to download the debian package: [Microsoft Online Apps](microsoft-online-apps.deb)

# Microsoft Fonts for Linux

Installing Microsoft TrueType Fonts on Ubuntu-based system adds the following fonts to LibreOffice:
ttf-mscorefonts-installer is V3.8.1ubuntu1 as of 2025-02-07 24.04 Ubuntu.

* Andale Mono
* Arial
* Arial Black
* Comic Sans MS
* Courier New
* Georgia
* Impact
* Times New Roman
* Trebuchet MS
* Verdana
* Windings

## Introduction

From: https://itsfoss.com/install-microsoft-fonts-ubuntu/

**Why are Microsoft fonts not installed by default in Linux?**

Times New Roman, Arial, and other such fonts are owned by Microsoft, and they are not open source. Many Linux distributions don’t provide proprietary software by default to avoid licensing issues. This is why Ubuntu and other Linux distributions use open-source fonts “Liberation fonts” to substitute Microsoft fonts by default.

The Liberation Fonts were created by Red Hat to substitute Arial, Arial Narrow, Times New Roman and Courier New as their width is the same. When you open a document written in Times New Roman, the equivalent Liberation Font will be used to keep the document uninterrupted.

However, Liberation fonts are not identical to Microsoft’s fonts and in some cases, you may need to use Arial or Times New Roman. A very common scenario is that Microsoft’s fonts are the only option in schools, universities and other public and private organizations. They require you to submit the documents in one of those fonts.

Good thing is that you can install the Microsoft fonts on Ubuntu and other distributions easily. This way, you will be able to increase the compatibility with LibreOffice and have the freedom to choose open-source office software. 

## Installation on Ubuntu

The multiverse repository is normally enabled. If not then `sudo add-apt-repository multiverse`

Install: `sudo apt update && sudo apt install ttf-mscorefonts-installer`

```
ian@hp:~$ sudo apt update && sudo apt install ttf-mscorefonts-installer
Hit:1 http://nz.archive.ubuntu.com/ubuntu noble InRelease                      
Hit:2 http://nz.archive.ubuntu.com/ubuntu noble-updates InRelease              
Hit:3 http://nz.archive.ubuntu.com/ubuntu noble-backports InRelease            
Hit:4 http://security.ubuntu.com/ubuntu noble-security InRelease               
Hit:5 https://esm.ubuntu.com/apps/ubuntu noble-apps-updates InRelease  
Hit:6 https://esm.ubuntu.com/apps/ubuntu noble-apps-security InRelease
Hit:7 https://esm.ubuntu.com/infra/ubuntu noble-infra-security InRelease
Hit:8 https://esm.ubuntu.com/infra/ubuntu noble-infra-updates InRelease
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
22 packages can be upgraded. Run 'apt list --upgradable' to see them.
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following package was automatically installed and is no longer required:
  libllvm17t64
Use 'sudo apt autoremove' to remove it.
The following additional packages will be installed:
  cabextract
The following NEW packages will be installed
  cabextract ttf-mscorefonts-installer
0 to upgrade, 2 to newly install, 0 to remove and 22 not to upgrade.
Need to get 50.3 kB of archives.
After this operation, 169 kB of additional disk space will be used.
Do you want to continue? [Y/n]

Get:1 http://nz.archive.ubuntu.com/ubuntu noble/universe amd64 cabextract amd64 1.11-2 [24.7 kB]
Get:2 http://nz.archive.ubuntu.com/ubuntu noble/multiverse amd64 ttf-mscorefonts-installer all 3.8.1ubuntu1 [25.6 kB]
Fetched 50.3 kB in 0s (120 kB/s)                     
Preconfiguring packages ...
Selecting previously unselected package cabextract.
(Reading database ... 384296 files and directories currently installed.)
Preparing to unpack .../cabextract_1.11-2_amd64.deb ...
Unpacking cabextract (1.11-2) ...
Selecting previously unselected package ttf-mscorefonts-installer.
Preparing to unpack .../ttf-mscorefonts-installer_3.8.1ubuntu1_all.deb ...
Unpacking ttf-mscorefonts-installer (3.8.1ubuntu1) ...
Setting up cabextract (1.11-2) ...
Setting up ttf-mscorefonts-installer (3.8.1ubuntu1) ...
Processing triggers for update-notifier-common (3.192.68build3) ...
ttf-mscorefonts-installer: processing...
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/andale32.exe
Get:1 http://downloads.sourceforge.net/corefonts/andale32.exe [198 kB]
Fetched 198 kB in 3s (76.0 kB/s)                                               
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/arial32.exe
Get:1 http://downloads.sourceforge.net/corefonts/arial32.exe [554 kB]
Fetched 554 kB in 2s (229 kB/s)                                                
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/arialb32.exe
Get:1 http://downloads.sourceforge.net/corefonts/arialb32.exe [168 kB]
Fetched 168 kB in 2s (70.2 kB/s)                                               
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/comic32.exe
Get:1 http://downloads.sourceforge.net/corefonts/comic32.exe [246 kB]
Fetched 246 kB in 2s (116 kB/s)                                                
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/courie32.exe
Get:1 http://downloads.sourceforge.net/corefonts/courie32.exe [646 kB]
Fetched 646 kB in 3s (231 kB/s)                                                
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/georgi32.exe
Get:1 http://downloads.sourceforge.net/corefonts/georgi32.exe [392 kB]
Fetched 392 kB in 2s (162 kB/s)                                                
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/impact32.exe
Get:1 http://downloads.sourceforge.net/corefonts/impact32.exe [173 kB]
Fetched 173 kB in 2s (74.3 kB/s)                                               
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/times32.exe
Get:1 http://downloads.sourceforge.net/corefonts/times32.exe [662 kB]
Fetched 662 kB in 3s (222 kB/s)                                                
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/trebuc32.exe
Get:1 http://downloads.sourceforge.net/corefonts/trebuc32.exe [357 kB]
Fetched 357 kB in 2s (173 kB/s)                                                
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/verdan32.exe
Get:1 http://downloads.sourceforge.net/corefonts/verdan32.exe [352 kB]
Fetched 352 kB in 3s (138 kB/s)                                                
ttf-mscorefonts-installer: downloading http://downloads.sourceforge.net/corefont
s/webdin32.exe
Get:1 http://downloads.sourceforge.net/corefonts/webdin32.exe [185 kB]
Fetched 185 kB in 2s (87.2 kB/s)                                               

These fonts were provided by Microsoft "in the interest of cross-
platform compatibility".  This is no longer the case, but they are
still available from third parties.

You are free to download these fonts and use them for your own use,
but you may not redistribute them in modified form, including changes
to the file name or packaging format.

Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/anda
le32.exe
  extracting fontinst.inf
  extracting andale.inf
  extracting fontinst.exe
  extracting AndaleMo.TTF
  extracting ADVPACK.DLL
  extracting W95INF32.DLL
  extracting W95INF16.DLL

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/aria
l32.exe
  extracting FONTINST.EXE
  extracting fontinst.inf
  extracting Ariali.TTF
  extracting Arialbd.TTF
  extracting Arialbi.TTF
  extracting Arial.TTF

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/aria
lb32.exe
  extracting fontinst.exe
  extracting fontinst.inf
  extracting AriBlk.TTF

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/comi
c32.exe
  extracting fontinst.inf
  extracting Comicbd.TTF
  extracting Comic.TTF
  extracting fontinst.exe

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/cour
ie32.exe
  extracting cour.ttf
  extracting courbd.ttf
  extracting courbi.ttf
  extracting fontinst.inf
  extracting couri.ttf
  extracting fontinst.exe

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/geor
gi32.exe
  extracting fontinst.inf
  extracting Georgiaz.TTF
  extracting Georgiab.TTF
  extracting Georgiai.TTF
  extracting Georgia.TTF
  extracting fontinst.exe

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/impa
ct32.exe
  extracting fontinst.exe
  extracting Impact.TTF
  extracting fontinst.inf

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/time
s32.exe
  extracting fontinst.inf
  extracting Times.TTF
  extracting Timesbd.TTF
  extracting Timesbi.TTF
  extracting Timesi.TTF
  extracting FONTINST.EXE

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/treb
uc32.exe
  extracting FONTINST.EXE
  extracting trebuc.ttf
  extracting Trebucbd.ttf
  extracting trebucbi.ttf
  extracting trebucit.ttf
  extracting fontinst.inf

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/verd
an32.exe
  extracting fontinst.exe
  extracting fontinst.inf
  extracting Verdanab.TTF
  extracting Verdanai.TTF
  extracting Verdanaz.TTF
  extracting Verdana.TTF

All done, no errors.
Extracting cabinet: /var/lib/update-notifier/package-data-downloads/partial/webd
in32.exe
  extracting fontinst.exe
  extracting Webdings.TTF
  extracting fontinst.inf
  extracting Licen.TXT

All done, no errors.
All fonts downloaded and installed.
Processing triggers for man-db (2.12.0-4build2) ...
Processing triggers for fontconfig (2.15.0-1.1ubuntu2) ...
ian@hp:~$ 
```

 The following two Package configuration messwage occur during installation...
```
 ┌─────────────────┤ Configuring ttf-mscorefonts-installer ├─────────────────┐
 │                                                                           │ 
 │ TrueType core fonts for the Web EULA                                        
 │                                                                             
 │ END-USER LICENSE AGREEMENT FOR MICROSOFT SOFTWARE                           
 │                                                                             
 │ IMPORTANT-READ CAREFULLY: This Microsoft End-User License Agreement         
 │ ("EULA") is a legal agreement between you (either an individual or a        
 │ single entity) and Microsoft Corporation for the Microsoft software         
 │ accompanying this EULA, which includes computer software and may include    
 │ associated media, printed materials, and "on-line" or electronic            
 │ documentation ("SOFTWARE PRODUCT" or "SOFTWARE"). By exercising your        
 │ rights to make and use copies of the SOFTWARE PRODUCT, you agree to be      
 │ bound by the terms of this EULA. If you do not agree to the terms of        
 │ this EULA, you may not use the SOFTWARE PRODUCT.                            
 │                                                                             
 │                                  <OK>                                       
 │                                                                           │ 
 └───────────────────────────────────────────────────────────────────────────┘ 


 ┌─────────────────┤ Configuring ttf-mscorefonts-installer ├─────────────────┐
 │                                                                           │ 
 │ In order to install this package, you must accept the license terms, the  │ 
 │ "TrueType core fonts for the Web EULA ". Not accepting will cancel the    │ 
 │ installation.                                                             │ 
 │                                                                           │ 
 │ Do you accept the EULA license terms?                                     │ 
 │                                                                           │ 
 │                    <Yes>                       <No>                       │ 
 │                                                                           │ 
 └───────────────────────────────────────────────────────────────────────────┘ 
      

```

## TFF's from the installation log are:

* AndaleMo.TTF
  
* Ariali.TTF
* * Arialbd.TTF
* * Arialbi.TTF
* Arial.TTF
* 
* AriBlk.TTF
* 
* Comicbd.TTF
* Comic.TTF
* 
* cour.ttf
* courbd.ttf
* courbi.ttf
* couri.ttf
* 
* Georgiaz.TTF
* Georgiab.TTF
* Georgiai.TTF
* Georgia.TTF
* 
* Impact.TTF
* 
* Times.TTF
* Timesbd.TTF
* Timesbi.TTF
* Timesi.TTF
* 
* trebuc.ttf
* Trebucbd.ttf
* trebucbi.ttf
* trebucit.ttf
* 
* Verdanab.TTF
* Verdanai.TTF
* Verdanaz.TTF
* Verdana.TTF
* 
* Webdings.TTF

* 
