# PC - General Setup and Settings

- Updated for Windows 11 22H2

# General Build Advice and Recommendations

- Consider in what order you should plug in fan and PSU wires versus installing the CPU cooler, based on the clearance and ease of building.
- Consider getting fan splitters and extensions to make it easier to install fans.

# General PC Build and First Boot Priority List

- **First, BACK UP EVERYTHING IMPORTANT TO AN EXTERNAL DRIVE (and ideally to the cloud as well)**
- [Create Windows 11 Installation Media on a USB Drive](https://www.microsoft.com/software-download/windows11) (NOTE: the USB drive will be wiped)
- Install ONLY a new/formatted SSD into the motherboard to be used as the main boot drive.
- Build the rest of the PC.
- Start up the PC, install and set up Windows.
- If necessary, transfer the Windows license by deactivating the old PC during setup, or via the Microsoft account management website.
- Update motherboard UEFI BIOS.
- Set up UEFI BIOS (see below).
- Update Windows.
- Update other drivers (CPU, GPU, audio (sometimes bundled with GPU drivers), etc.).
- Set up Windows accordingly and install other system software.
- Turn off the PC, open it up again, then mount the old SSD as a media drive in another M.2 slot.
- Copy over and back up the important files from the media drive to the main drive.
- Proceed with the rest of setup.
- Once absolutely certain that nothing has been missed, format the media drive, then drag over the backed up content onto the newly formatted drive.

# General File Organization, ETC

- Store normally installed games and other software on the main system drive.
- Store media, documents, portable apps/games, and other stuff on the secondary media drive (ex. "My Photos", "My Videos", "My Documents", "My Software", etc.).

## Windows Explorer

- View > Show > CHECK: "File name extensions"; "Hidden items"
- (To change the default view for a type of folder) (In template folder with desired default view) Options > View > Folder views: Apply to Folders
- Pin folders to Quick Access as desired.
- (Optional) Right-click the Downloads folder > Properties > Location > Set accordingly to point at the appropriate folder on the appropriate drive (NOTE: not recommended to remap other User folders that could get cluttered by system/application files being saved there by default, such as Pictures and Documents. Instead, manually point applications to save to those alternate folders when needed.)
- (Optional) Options > View > Navigation pane > CHECK: "Show libraries" > (For each Library) Right-click each Library folder > Properties > Library locations > Set accordingly to include the appropriate folders on the appropriate drives (ex. setting Pictures and Videos to include "My Photos" and "My Videos" on the secondary media drive).
- (Optional) View > Show > CHECK: "Details Pane"

# UEFI BIOS Setup

- Ideally, update the BIOS at least once, when you first boot with the motherboard in a new build.
- DISABLE Fast Boot (Fast Boot is not as beneficial with an SSD, and it can cause issues).
- ENABLE XMP/DOCP/EOCP to set RAM speeds to the advertised values (to be safe, do not exceed those advertised values).

# System/Driver Updates, ETC

- Download and install all necessary OS updates.
- Download and install all necessary drivers and driver updates for CPU, GPU, audio, etc.

# Windows Power Settings

## Windows Control Panel

- Power Options > Choose appropriate power plan (typically Balanced)
- Power Options > Choose what the power buttons do > "Turn on fast startup": DISABLED (also see UEFI BIOS Setup above)

# Monitor Setup (Refresh Rate, Adaptive Sync, ETC)

## Monitor OSD Menu

- Calibrate the monitor.
- Toggle/change any necessary settings (Adaptive Sync, etc.).

## NVidia Control Panel

- Display > Change resolution (change if necessary)
- **(If using Adaptive Sync) Display > Set up G-SYNC > Apply following changes > CHECK: "Enable G-SYNC, G-SYNC Compatible": "Enable for full screen mode" (NOTE: Even with the Windows "Optimizations for windowed games" setting on, still keep this on full screen mode only)**
- Select each display > CHECK: "Enable settings for the selected display model" > Apply

## Windows Settings

- System > Display > Arrange displays as necessary
- System > Display > Display resolution > Set accordingly
- System > Display > Scale > Set accordingly
- System > Display > Advanced display > Set the screen refresh rate of the monitor(s)
- System > Display > Graphics > Change default graphics settings > CHECK: Optimizations for windowed games

# Local Group Policy Editor Settings (Windows Pro Only)

## Disable Windows Automatic Updates and Restarting

- Computer Configuration > Administrative Templates > Windows Components > Windows Update > Manage end user experience > Configure Automatic Updates: ENABLED > Options: "3 - Auto download and notify for install" > UNCHECK: "install during automatic maintenance"

## Enable Long File Paths

- Computer Configuration > Administrative Templates > System > Filesystem > “Enable Win32 long paths”: ENABLED
- NOTE: This will not fix all issues with long file paths, as the long path support works in some contexts but not in others (ex. Windows File Explorer might still have issues when trying to move or copy/paste files).
- If having issues with manipulating files with long path names, try using 7-Zip or Robocopy.

# Personalization, Privacy, ETC

- Download and set up Open-Shell Menu

## Windows Settings

- System > Display > Night light > Schedule night light > Customize as desired
- System > Notifications > Turn on do not disturb automatically > Customize as desired
- System > Notifications > Set priority notifications > Customize as desired (NOTE: Certain notifications, such as from YouTube, are "reminders", and will not auto-dismiss by default. Consider disabling "Show reminders, regardless of app used")
- System > Focus > Customized as desired
- **System > Nearby sharing > Nearby sharing: OFF**
- System > Multitasking > Snap Windows > UNCHECK: "When I drag a window, let me snap it without dragging all the way to the screen edge"
- System > Multitasking > Snap Windows > Customize as desired
- System > Multitasking > Show Microsoft Edge tabs when snapping or pressing Alt + Tab: "Don't show tabs"
- **System > Multitasking > Desktops > On the taskbar, show all the open windows: "Only on the desktop I'm using"**
- **System > Multitasking > Desktops > Show all open windows when I press Alt+Tab: "Only on the desktop I'm using"**
- System > Multitasking > Alt + Tab > Customize as desired
- **System > Clipboard > Clipboard history: ON**
- **System > Clipboard > Sync across your devices: OFF**
- Personalization > Background > Customize as desired
- Personalization > Colors > Customize as desired
- Personalization > Themes > Customize as desired
- Personalization > Themes > Desktop icon settings > UNCHECK: Recycle Bin (pin it to Start Menu and/or Quick Access first, for easy access)
- Personalization > Start > Layout: More pins
- Personalization > Start > Show recently added apps: OFF
- Personalization > Start > Show most used apps: OFF
- **Personalization > Start > Show recently opened items in Start, Jump lists, and File Explorer: OFF (see: Lauren Iroas scandal :^) )**
- Personalization > Start > Folders > Customize as desired
- Personalization > Taskbar > Customize as desired
- **Personalization > Taskbar > Taskbar behaviors > When using multiple displays, show my taskbar apps on: "Main taskbar and taskbar where window is open"**
- Personalization > Taskbar > Taskbar behaviors > UNCHECK: "Select the far corner of the taskbar to show the desktop"
- **Personalization > Device usage > UNCHECK all, or as necessary**
- Accounts > Sign-in options > Customize as desired
- **Accounts > Windows backup > Remember my apps: OFF**
- **Accounts > Windows backup > Remember my preferences: OFF**
- **Gaming > Xbox Game Bar shortcut: OFF**
- **Gaming > Captures > Record what happened: OFF**
- **Gaming > Game Mode > Game Mode: OFF** (may reduce unneeded throttling on background apps)
- Accessibility > Visual effects > Customize as desired
- **Privacy & security > General > UNCHECK all, or as necessary**
- **Privacy & security > Diagnostics & feedback > UNCHECK all, or as necessary**
- **Privacy & security > Activity History > UNCHECK: "Store my activity history on this device"** (on Windows 10, this also disables the Timeline in Task View (Win+Tab))
- **Windows Update > Advanced Options > Delivery Optimization > Allow downloads from other PCs: OFF**

## Control Panel

- **File Explorer Options > General > Privacy > UNCHECK: "Show recently used files in Quick access"; "Show frequently used folders in Quick access"**

### Windows 10 Taskbar Settings (Deprecated)

- Personalization > Taskbar > Taskbar location on screen: Right
- Personalization > Taskbar > Combine taskbar buttons: Always, hide labels
- Personalization > Taskbar > Multiple displays > Show taskbar buttons on: Main taskbar and taskbar where window is open
- Personalization > Taskbar > Multiple displays > Combine buttons on other taskbars: Always, hide labels

## Setting Custom Event/Notification Sounds

- Convert the sound(s) you wish to use to WAV format.
- Move the sounds to C:\Windows\Media.
- Control Panel > Sound > Sounds > Select the appropriate sound for the event you wish to use it for, and click Apply.

# Mouse, Keyboard, Language, ETC

- Install the [Google Japanese IME](https://www.google.co.jp/ime/).

## Windows Settings

- **Time & language > Typing > Autocorrect misspelled words: OFF**
- **Time & language > Typing > Advanced keyboard settings > Override for default input method > Select: "Japanese - Google Japanese Input"**
- **Time & language > Typing > Advanced keyboard settings > Input language hot keys > Change Key Sequence... > Change all to: "Not Assigned"**
- **Accessibility > Keyboard > Sticky, Filter, and Toggle keys: OFF for all (also go into their individual settings and disable their keyboard shortcuts)**
- **Accessibility > Narrator > Keyboard shortcut for Narrator: OFF**

## Control Panel

- Mouse > Pointer Options > Motion > Pointer speed: 6/11 (middle; raw input)
- Mouse > Pointer Options > Motion > Uncheck: "Enhance pointer precision" (disables mouse acceleration)

# Date, Time, ETC

## Control Panel

- Date and Time > Additional Clocks > Add as necessary
- Region > Formats > Short date: yyyy-MM-dd
- Region > Formats > Long date: dddd, MMMM d, yyyy
- Region > Formats > Short time: HH:mm
- Region > Formats > Long time: HH:mm:ss
- Region > Formats > First day of week: Monday

# Network and Internet

## Change DNS

- [Cloudflare 1.1.1.1](https://1.1.1.1/dns/)

## Flushing the DNS Cache (If Having Issues)

- Open Terminal > ENTER: "ipconfig/flushdns"

## Checking Ping/Latency

- Open Resource Monitor > Network > CHECK: name of application/executable > TCP Connections > Check the Packet Loss and Latency sections
- (If you have a specific IP address to test) Open Terminal > ENTER: "ping (IP Address)" > ENTER: "tracert (IP Address)" > ENTER: "pathping (IP Address)"

# Enabling/Disabling Startup Apps, Removing Bloatware, ETC

- [Add an app to run automatically at startup in Windows 10](https://support.microsoft.com/en-us/windows/add-an-app-to-run-automatically-at-startup-in-windows-10-150da165-dcd9-7230-517b-cf3c295d89dd)
- Remove/uninstall any preinstalled bloatware on the Start Menu as desired.

## Windows Settings

- Apps > Startup > UNCHECK any apps you don't want/need to run at startup

# Disk Cleanup and Maintenance

## Disk Cleanup

- (Periodically) Open Disk Cleanup > Select: "Clean up system files" > CHECK: "previous Windows installations" > Run

## Windows Settings

- System > Storage > Storage Sense > ENABLE: Cleanup of temporary files
- **System > Storage > Storage Sense > Automatic User content cleanup: OFF**

# Other Windows Setup

- Install [WSL (Windows Subsystem for Linux)](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

# Fix Incorrect Application DPI Scaling

- Right-click application icon in task bar > Right-click application name in the menu > Properties > Compatibility > Change high DPI settings > High DPI Scaling Override > CHECK: "Scaling performed by: Application"

# Fix .jpg files getting saved as .jfif

- Run Registry Editor > Navigate to "HKEY_CLASSES_ROOT\MIME\Database\Content Type\image/jpeg"
- Extension > Value data > change from ".jfif" to ".jpg"

# Overclocking, Undervolting, ETC

## MSI Afterburner + RTSS (RivaTuner Statistics Server)

### Afterburner

- Note: OC Scanner no longer recommended due to lack of support
- [MSI Afterburner OC Scanner Setup](https://www.msi.com/blog/get-a-free-performance-boost-with-afterburner-oc-scanner).
- NVidia Control Panel > Desktop > CHECK: "Enable Developer Settings"
- NVidia Control Panel > Developer > Manage GPU Performance Counters > CHECK: "Allow access to the GPU performance counters to all users"
- MSI Afterburner Settings > General > CHECK: "Start with Windows"; "Start minimized"
- MSI Afterburner Settings > Compatibility properties > CHECK: "Unlock voltage control"; "Unlock voltage monitoring"
- Slide Core Voltage (if applicable), Power Limit, and Temp Limit to max > Apply
- Click the OC Scanner icon > Scan > Test > Apply > Save profile
- Click "Apply at Windows Startup" (the Windows icon)

### RTSS

- CHECK: "Start with Windows"
- Add game profiles as necessary to enable the OSD and/or set framerate limits (Ctrl + Left-click on "Add" to create a profile for a running application)
- If having issues with other applications that are trying to hook into the game (OBS streaming, Discord streaming, etc.), try adding the game as an exception to RTSS with "Application detection level > None"

## Intel XTU (Extreme Tuning Utility) OR AMD Ryzen Master

- https://www.intel.com/content/www/us/en/gaming/resources/overclocking-xtu-guide.html

## Fan Control (Rem0o)

- https://www.youtube.com/watch?v=uDPKVKBMQU8

## OCCT

#pc
#settings
