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

The V2.0 `microsoft-online-apps.deb` file is in this papanui repository in the [ms_apps](./ms_apps) folder.

Click to get to the github page to download the debian package: [Microsoft Online Apps](microsoft-online-apps.deb)

