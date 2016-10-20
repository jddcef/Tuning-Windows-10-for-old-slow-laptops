# Tuning Windows 10 for Slow Machines

![Windows 10 on slow netbook](http://i.ebayimg.com/00/s/MTIwMFgxNjAw/z/nHoAAOSwDNdVvxgT/$_57.JPG)

This guide is for those who dares to install Windows 10 on slow netbooks (1GB of RAM).  
Though Windows update program is over, you still may use old Windows product keys from license stickers to install Windows 10 on old machines.

## Explanations

* `Win + R` -- Press and hold _"Windows"_ key, then press key R, then relese both keys.
* `Search "FooBar"`  -- Click searching glass icon in taskbar or click Windows Start icon and start typing FooBar. You don't need to type all the phrase, only the beginning. 

## Table of Contents

Windows 10 Performance Checklist:
  0. [Reset Windows (Advanced)](#0-reset-windows-advanced)
  1. [Remove Unnecessary Apps/Crapware/Bloatware](#1-remove-unnecessary-appscrapwarebloatware)
  2. [Clean System from Viruses/Malware/Adware, etc.](#2-clean-system-from-virusesmalwareadware-etc)
  3. [Remove Some Apps from Autorun](#3-remove-some-apps-from-autorun)
  4. [Leave Enough Free Space on Your Drives for Windows 10](#4-leave-enough-free-space-on-your-drives-for-windows-10)
  5. [Tweak Visual Effects](#5-tweak-visual-effects)
  6. [Turn Off System Protection on Disks](#6-turn-off-system-protection-on-disks)
  7. [Opt Out from Privacy Options](#7-opt-out-from-privacy-options)
  8. [Turn Off Windows Components](#8-turn-off-windows-components)
  9. [Tweak Windows Services (Advanced)](#9-tweak-windows-services-advanced)
  10. [Tweak Your Browser](#10-tweak-your-browser)
  11. [Defragment Your HDDs](#11-defragment-your-hdds)
  12. [Unplug or Turn Off Unnecessary Devices](#12-unplug-or-turn-off-unnecessary-devices)
  13. [Tweak Power Options (Doubtful)](#13-tweak-power-options-doubtful)

If Nothing Helps:
  1. [Check HDD, FileSystem and Windows Files for Errors (Advanced)](#1-check-hdd-filesystem-and-windows-files-for-errors-advanced)
  2. [Install Other OS. Upgrade Hardware](#2-install-other-os-upgrade-hardware)

## Windows 10 Performance Checklist

### 0. Reset Windows (Advanced)

If you don't mind uninstalling all your programs, move all your precious data to other partition than `C:`.  
Then you may restore Windows into the _"just installed"_ state with `Search "Recovery options" > Reset this PC > Remove Everything > Only the drive where windows is installed`.  
After install you will have to reconfigure Windows and install all necessary programs like file archivator.  
Read more:
  * [techrepublic](http://www.techrepublic.com/article/reset-your-windows-10-system-with-the-remove-everything-option)
  * [laptopmag]( http://www.laptopmag.com/articles/reset-windows-10-pc )

### 1. Remove Unnecessary Apps/Crapware/Bloatware
* New way: `Search "Apps & features"` or `Settings > System > Apps & features > Click an app > Uninstall`
* Old way: `Win + R > appwiz.cpl`
* [Farbar Recovery Scan Tool][FarBar] (advanced)

### 2. Clean System from Viruses/Malware/Adware, etc.

You may use these programs:
  1. __Free Anti-adware (Not Antiviurses)__
    * [AdwCleaner](https://toolslib.net/downloads/viewdownload/1-adwcleaner)
    * [Malwarebytes Anti-Malware](https://www.malwarebytes.com)
    * [Farbar Recovery Scan Tool][FarBar]
  2. __Free Antiviruses__
    * [Avira](https://avira.com)
    * [Avast](https://avast.com) or [Avast for Business (no ads, but advanced)](https://business.avast.com)
    * Weak but fast Windows Defender + `Settings > Devices > AutoPlay > OFF "Use AutoPlay..."`
    * Others: https://www.av-comparatives.org

### 3. Remove Some Apps from Autorun
* `Ctrl + Shift + Esc > More details > Startup > Right click > Disable`
* Additionaly you may use [Autoruns tool by SysInternals](https://technet.microsoft.com/en-us/sysinternals/bb963902.aspx) or [CCleaner]

### 4. Leave Enough Free Space on Your Drives for Windows 10
Subjectivly I think 10GB is enough for Winfows 10 to function properly. [PC Advisor] recommends to keep 10% of each volume free.  
You may free up disk space by running these tools:
  * `Search "Disk Cleanup" > Right Click > Run as administrator` or `Win + R > cleanmgr`
  * [CCleaner]

[FarBar]: http://www.geekstogo.com/forum/topic/335081-frst-tutorial-how-to-use-farbar-recovery-scan-tool
[CCleaner]: https://www.piriform.com/ccleaner

### 5. Tweak Visual Effects
* `Search "advanced system settings" > Performance Settings > Adjust for best performance`
* `Settings > Personalization > Colors > OFF "Make Start, taskbar... transparent" and OFF others of your choice`
* `Settings > Ease of Access > Other options > OFF "Play animation" and OFF "Show background"`
* Unpin all tiles from Start Menu and shrink it.

### 6. Turn Off System Protection on Disks
System protection feature tells Windows to record changes made during software installations for purpose of rolling back when system fails to operate. If you feel brave, you may turn it off:  
`Search "advanced system settings" > Choose disk > Configure > Disable`

### 7. Opt Out from Privacy Options

`Settings > Privacy >`:
  * `General > OFF "Send Microsoft info about how I write..." and OFF others of your choice`
  * `Speech, inking and typing > Stop getting to know me`
  * `Location > Change > OFF` if you don't need location tracking
  * `Background apps > OFF all except "Settings"`

### 8. Turn Off Windows Components
* [Disable OneDrive](http://www.howtogeek.com/225973/how-to-disable-onedrive-and-remove-it-from-file-explorer-on-windows-10)
* [Disable Cortana](http://www.howtogeek.com/265027/how-to-disable-cortana-in-windows-10)
* `Settings > System > Notifications & actions > Show me tips about Windows > OFF`
* `Win + R > appwiz.cpl > Turn Windows feartures on or off` (advanced)

### 9. Tweak Windows Services (Advanced)

Open services by `Win + R > services.msc`. There you may change some services from automatic startup to manual (when needed) or turn off services completely. If you turn off some important services your system may become unfunctional. You may get some insight from [Black Viper manual](http://www.blackviper.com/service-configurations/black-vipers-windows-10-service-configurations).

I usually set as manual services (but don't trust me: I have little experience): Themes, IP Helper (I don't use IPv6), TCP/IP NetBIOS Helper (I don't use local network), Fax, Print Spooler (I don't use printers/fax).

### 10. Tweak Your Browser
* Remove unnecessary browser extensions and apps, disable unused features ([in Chrome](https://support.google.com/chrome_webstore/answer/2664769))
* Install fast adblocker ([uBlock Origin for Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm), Opera and [Brave](https://brave.com) have built in adblcokers [enable in settings])
* [Disable autorun for plugins (like Flash)](http://www.pcworld.com/article/2858421/internet/how-to-stop-autoplay-videos.html)
* Disable HTML5 media content (advanced, e.g. block requests of type "Other" in [uMatrix](https://chrome.google.com/webstore/detail/umatrix/ogfcmafjalglgifnmanfmnieipoejdcf))

### 11. Defragment Your HDDs

`Search "Defragment and Optimize Drives"`  
You may read more about [defragmentation](http://lifehacker.com/5976424/what-is-defragging-and-do-i-need-to-do-it-to-my-computer) on the internets.

### 12. Unplug or Turn Off Unnecessary Devices

`Win + R > ncpa.cpl > Right click on unused network interface > Disable`

### 13. Tweak Power Options (Doubtful)

I doubt this option, but some resources mention it:  
`Search "Power Options" > Show additional plans > High performance`

## If Nothing Helps

### 1. Check HDD, FileSystem and Windows Files for Errors (Advanced)

If your HDD is old it may slow down the whole system, however it may be checked and healed.

1. Find HDD diagnosic tool (SMART may be used) and check drive's health, e.g. [MHDD](http://hddguru.com/software/2005.10.02-MHDD) is an old tool for advanced users.
2. Remap bad or slow HDD sectors, e.g. [Low Level Format Tool](http://hddguru.com/software/HDD-LLF-Low-Level-Format-Tool) remaps slow sectors while deleting all data.
3. Fix filesystem errors, e.g. with `Win + R > cmd.exe > CHKDSK C: /F`
4. Fix corruped Windows files: `Win + R > cmd.exe > sfc /scannow` ([details](http://www.howtogeek.com/howto/windows-vista/verify-the-integrity-of-windows-vista-system-files))

### 2. Install Other OS or Upgrade Hardware

You may install Windows 7, lightweight Linux (e.g. [Lubuntu](http://lubuntu.net)), [CloudReady](https://www.neverware.com) or Android for PC ([RemixOS](http://www.jide.com/remixos), [PhoenixOS](http://www.phoenixos.com), [Android-x86](http://android-x86.org)).
Or you may add more RAM, switch to SSD, upgrade other hardware or buy a new notebook.

# Sources

* [PC Advisor: How to speed up Windows 10][PC Advisor]
* [Make Use Of: How to Speed Up Windows 10 From Boot to Shut Down][Make Use Of]
* [CNET: 6 easy ways to speed up Windows 10][CNET]
* [Softpedia: Three Ways to Make the Windows 10 Start Menu a Lot Faster][Softpedia]
* [IT PRO: How to speed up Windows 10][IT PRO]
* [PC World: How to make Windows 10 faster: 5 ways to speed up your PC][PC World]

[PC Advisor]: http://www.pcadvisor.co.uk/how-to/windows/how-speed-up-windows-10-how-make-windows-10-faster-3631916
[Make Use Of]: http://www.makeuseof.com/tag/speed-windows-10-boot-shut
[CNET]: https://www.cnet.com/how-to/6-easy-ways-to-speed-up-windows-10
[Softpedia]: http://news.softpedia.com/news/three-ways-to-make-the-windows-10-start-menu-a-lot-faster-490584.shtml
[IT PRO]: http://www.itpro.co.uk/operating-systems/26138/how-to-speed-up-windows-10-2
[PC World]: http://www.pcworld.com/article/3030200/windows/how-to-make-windows-10-faster-5-ways-to-speed-up-your-pc.html

---------------------------

Short URL: https://git.io/boost-win10 | [Github's Gists LACK COMMENT NOTIFICATIONS](https://github.com/isaacs/github/issues/21)