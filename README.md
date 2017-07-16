# FlashAir FileManager

This FileManager is based on:
  * The FlashAir Example code available from 
    https://flashair-developers.com/en/documents/tutorials/advanced/2/
  * The used API is described on
    https://flashair-developers.com/en/documents/api/
  * The FileManger build by https://github.com/luc-github/Flashair-FM
  * And the following libraries are used
    * jQuery JavaScript Library https://jquery.com/ https://github.com/jquery/jquery
	* Bootstrap HTML/CSS responsive framework http://getbootstrap.com/ https://github.com/twbs/bootstrap
	* "Growl-like" notifications for Bootstrap http://bootstrap-notify.remabledesigns.com/ https://github.com/mouse0270/bootstrap-notify
	* A cross-browser library of CSS animations (used for notifications) http://daneden.github.io/animate.css https://github.com/daneden/animate.css
 
## User Interface

TODO

## Features

It allows to browse, upload and delete files on SD Card and to know the current capacity of the Card.

## Configuration

 1. Backup the content of SD_WLAN of your SD Card - just in case
 2. Add/Replace the content of SD_WLAN by the one from this repository 
 3. Edit the CONFIG based on your network - I have prepared CONFIG-SAMPLE, it joins existing network - just need to complete SSID/Password and Name    
    * `APPMODE=5` Autostart WLAN mode and configure it to join an existing Network (STA mode)
	* `APPSID` defines the WLAN SSID to join and `APPNETWORKKEY` is the password
	* `DELCGI=/thumbnail.cgi,/config.cgi` disables the cgi scripts to view thumbnails or to configure the settings via browser
	* `WEBDAV=0` disabled the WebDAV drive like features
	* `UPLOAD=1` enables upload via browser
	* For more information please check: https://flashair-developers.com/en/documents/api/config/

```
APPMODE=5   
APPSSID=<Your-SSID>   
APPNETWORKKEY=<Your-Password>   
APPNAME=<YourName>  
DELCGI=/thumbnail.cgi,/config.cgi
WEBDAV=0
UPLOAD=1
```

 4. you can edit the List.htm to change the header
```
   <h1>Wifi SD Card</h1>
```
 
 5. Unplug and replug card to refresh settings
