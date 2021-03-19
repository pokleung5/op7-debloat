# op7-debloat

``` bash
# list all system app
pm list package -s | sort
# list all running app
OnePlus7:/ $ ps -A | grep [.].*[.] | awk '{print $9}' | grep -v @ | sort -u
# uninstall app
pm uninstall --user 0 <package>
# disable app
pm disable-user --user 0  <package>
# reinstall 
pm enable <package>
cmd package install-existing <package>
```

## Thinking
1. Non running app is safe to uninstall 
2. Do not touch qualcomm app
3. `ps -A` can also list the user running id
4. Unbrick tools works: https://forum.xda-developers.com/t/op7-oos-10-3-8-gm57aa-0-10gm57ba-unbrick-tool-to-restore-your-device-to-oxygenos.3954325/


## experience
### Keep:
```
com.google.android.documentsui
net.oneplus.launcher
com.google.android.modulemetadata
```
## if you need profile, keep these
```
com.oneplus.contacts
com.oneplus.contacts.basiccolorblack.overlay
com.oneplus.contacts.basiccolorwhite.overlay
```
### Not sure:
```
com.example.tmo
com.example.wifirftest
com.fingerprints.fingerprintsensortest
com.google.android.apps.walletnfcrel
com.google.android.modulemetadata
com.google.android.printservice.recommendation
com.google.android.setupwizard
com.oneplus.asti
com.oneplus.coreservice
com.oneplus.diagnosemanager
com.oneplus.geoiptime
com.oneplus.ifaaservice
com.oneplus.overlay
com.oneplus.sdcardservice
com.oneplus.security
com.oneplus.setupwizard
com.oneplus.simcontacts
com.oneplus.sms.smscplugger
com.tencent.soter.soterserver
```
### Before uninstall any app, use a trust PC to always access `adb shell` even during boot loop

## List (Please think before running any script)
```
pm uninstall --user 0 cn.oneplus.nvbackup
pm uninstall --user 0 cn.oneplus.oemtcma
pm uninstall --user 0 cn.oneplus.opmms  
pm uninstall --user 0 cn.oneplus.photos 
pm uninstall --user 0 com.android.bookmarkprovider
pm uninstall --user 0 com.android.chrome
pm uninstall --user 0 com.dsi.ant.server
pm uninstall --user 0 com.google.android.apps.docs
pm uninstall --user 0 com.google.android.apps.maps
pm uninstall --user 0 com.google.android.apps.photos
pm uninstall --user 0 com.google.android.apps.restore
pm uninstall --user 0 com.google.android.apps.tachyon
pm uninstall --user 0 com.google.android.apps.turbo
pm uninstall --user 0 com.google.android.apps.wellbeing
pm uninstall --user 0 com.google.android.as
pm uninstall --user 0 com.google.android.calendar
pm uninstall --user 0 com.google.android.feedback
pm uninstall --user 0 com.google.android.gm
pm uninstall --user 0 com.google.android.gms.location.history
pm uninstall --user 0 com.google.android.googlequicksearchbox
pm uninstall --user 0 com.google.android.marvin.talkback
pm uninstall --user 0 com.google.android.music
pm uninstall --user 0 com.google.android.projection.gearhead
pm uninstall --user 0 com.google.android.videos
pm uninstall --user 0 com.google.android.youtube
pm uninstall --user 0 com.google.ar.core
pm uninstall --user 0 com.oem.autotest
pm uninstall --user 0 com.oem.logkitsdservice
pm uninstall --user 0 com.oem.nfc
pm uninstall --user 0 com.oem.oemlogkit
pm uninstall --user 0 com.oem.rftoolkit
pm uninstall --user 0 com.oneplus.account
pm uninstall --user 0 com.oneplus.account.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.account.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.backuprestore
pm uninstall --user 0 com.oneplus.brickmode
pm uninstall --user 0 com.oneplus.bttestmode
pm uninstall --user 0 com.oneplus.calculator
pm uninstall --user 0 com.oneplus.calculator.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.calendar
pm uninstall --user 0 com.oneplus.calendar.black.overlay
pm uninstall --user 0 com.oneplus.calendar.white.overlay
pm uninstall --user 0 com.oneplus.camera
pm uninstall --user 0 com.oneplus.camera.resources
pm uninstall --user 0 com.oneplus.camera.service
pm uninstall --user 0 com.oneplus.card
pm uninstall --user 0 com.oneplus.card.black.overlay
pm uninstall --user 0 com.oneplus.card.white.overlay
pm uninstall --user 0 com.oneplus.cloud
pm uninstall --user 0 com.oneplus.cloud.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.cloud.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.contacts
pm uninstall --user 0 com.oneplus.contacts.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.contacts.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.deskclock
pm uninstall --user 0 com.oneplus.deskclock.black.overlay
pm uninstall --user 0 com.oneplus.deskclock.white.overlay
pm uninstall --user 0 com.oneplus.faceunlock
pm uninstall --user 0 com.oneplus.filemanager
pm uninstall --user 0 com.oneplus.filemanager.black.overlay
pm uninstall --user 0 com.oneplus.filemanager.white.overlay
pm uninstall --user 0 com.oneplus.gallery
pm uninstall --user 0 com.oneplus.gamespace
pm uninstall --user 0 com.oneplus.gamespace.black.overlay
pm uninstall --user 0 com.oneplus.gamespace.white.overlay
pm uninstall --user 0 com.oneplus.houston
pm uninstall --user 0 com.oneplus.mms
pm uninstall --user 0 com.oneplus.mms.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.mms.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.note
pm uninstall --user 0 com.oneplus.note.black.overlay
pm uninstall --user 0 com.oneplus.note.white.overlay
pm uninstall --user 0 com.oneplus.opbackup
pm uninstall --user 0 com.oneplus.opbackup.black.overlay
pm uninstall --user 0 com.oneplus.opbackup.white.overlay
pm uninstall --user 0 com.oneplus.opbugreportlite
pm uninstall --user 0 com.oneplus.opsports
pm uninstall --user 0 com.oneplus.opsports.black.overlay
pm uninstall --user 0 com.oneplus.opsports.white.overlay
pm uninstall --user 0 com.oneplus.opwlb
pm uninstall --user 0 com.oneplus.opwlb.black.overlay
pm uninstall --user 0 com.oneplus.opwlb.white.overlay
pm uninstall --user 0 com.oneplus.screenrecord
pm uninstall --user 0 com.oneplus.screenrecord.black.overlay
pm uninstall --user 0 com.oneplus.screenrecord.white.overlay
pm uninstall --user 0 com.oneplus.ses
pm uninstall --user 0 com.oneplus.soundrecorder
pm uninstall --user 0 com.oneplus.soundrecorder.black.overlay
pm uninstall --user 0 com.oneplus.soundrecorder.white.overlay
pm uninstall --user 0 com.oneplus.twspods
pm uninstall --user 0 com.recognize.number
pm uninstall --user 0 net.oneplus.commonlogtool
pm uninstall --user 0 net.oneplus.forums
pm uninstall --user 0 net.oneplus.odm
pm uninstall --user 0 net.oneplus.odm.provider
pm uninstall --user 0 net.oneplus.push
pm uninstall --user 0 net.oneplus.weather
pm uninstall --user 0 net.oneplus.weather.basiccolorblack.overlay
pm uninstall --user 0 net.oneplus.weather.basiccolorwhite.overlay
pm uninstall --user 0 net.oneplus.widget
```
