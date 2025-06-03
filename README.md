## USB Creator  Pro

USB Creator Pro is a modified version of the [Chromebook Recovery Utility](https://chromewebstore.google.com/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm?hl=en) used to recover Chromebooks in an inoperable state.  USB Creator Pro allows the use of a remote file specifying available images, allowing (format described below). USB Creator Pro also allows the use of 'bin', 'zip', 'tar', 'xz', 'iso' , and  'img' file types without renaming.

## Remote Image Server Confirguration

You can change the location of the image server by modifying the following line in app\_compiled-bundle.js

```javascript
function getAppConfigForOnHub_() {
 return {
   messageCatalogPostfix: '_ON_HUB',
   recovery_config_urls: [
     'https://raw.githubusercontent.com/dismal002/usbtool/refs/heads/main/onhu>
   ],
```
This is the format that should be used on the remote server note that the zipfilesize and filsize checks are not case sensitive.
```json
[
 {
   "channel": "stable-channel",
   "desc": "",
   "filesize": 861,
   "file": "android-x86-7.1-r1.iso",
   "hwidmatch": "^GARE .*",
   "manufacturer": "Android x86",
   "model": "Android x86 7.1",
   "name": "Android x86 7.1",
   "photourl": "",
   "sku": "",
   "zipfilesize": 861,
   "url": "https://osdn.net/projects/android-x86/downloads/67834/android-x86-7.1-r1.iso/",
   "hwids": []
 }
]
```
