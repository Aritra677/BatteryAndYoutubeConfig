# BatteryAndYoutubeConfig
  -----------------------

These are config files for battery using tlp which is meant to work in  arch/debian/void or any other minimial setup distro out of the box for 12 amd 13th gen i3/i5/i7 processors with igpu this doesn't contain controls for external gpu's but h series processors of the i5 and i7 will work especially h series processor laptops with igpu's thin and light series ones like the hp pavillion/omnibook or acer aspire / asus vivobook series as examples ... 

-----------One thing to keep in mind all configuration changes made here are for from my studies if any further improvements are meant to be made feel free to correct me ..........


One thing to make sure these will work best on any glibc based distros this is mainly a warning for the tlp config since media drivers often don't go very well with musl based distros like in void musl or perhaps alpine so it's better to check your distros libc version and type although tlp shouldn't be an issue here !!


Now regarding where to make what changes --->

For youtube video watching using terminal we need mpv , yt-dlp to be installed first and intel media drivers package should be named as intel-media-driver and some other packages include libva and libva-utils as named with mesa / mesa-va-drivers which provide user-space graphics support .Here libva-utils is for debugging via vainfo and libva is the core video accelaration API library here .
Installation may depend based on distro like 

For Debian ---->
-------------------------

  sudo apt update && sudo apt install mpv yt-dlp intel-media-va-driver libva2 libva-utils mesa-va-drivers
  
For Arch  ------>
-------------------------

  sudo pacman -Syu intel-media-driver libva-utils libva-mesa-driver mpv yt-dlp
  
 For Void ------->
 ------------------------
 
   sudo xbps-install -S intel-media-driver libva-utils mesa-vaapi mpv yt-dlp
