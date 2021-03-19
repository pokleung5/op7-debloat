# op7-debloat

``` bash
# list all system app
pm list package -s | sort
# list all running app
ps -A | grep [.].*[.]
```

## Thinking:
1. Non running app is safe to uninstall 
2. Do not touch qualcomm app
3. `ps -A` can also list the user running id
4. Reboot will auto reinstall all system app, so should be safe even uninstalled wrong app
5. Unbrick tools works: https://forum.xda-developers.com/t/op7-oos-10-3-8-gm57aa-0-10gm57ba-unbrick-tool-to-restore-your-device-to-oxygenos.3954325/

## List (Please think before running any script)
```
pm uninstall --user 0 cn.oneplus.nvbackup
pm uninstall --user 0 cn.oneplus.oemtcma
pm uninstall --user 0 cn.oneplus.opmms
pm uninstall --user 0 cn.oneplus.photos
pm uninstall --user 0 com.oneplus.asti
pm uninstall --user 0 com.oneplus.faceunlock
pm uninstall --user 0 com.oneplus.geoiptime
pm uninstall --user 0 com.oneplus.houston
pm uninstall --user 0 com.oneplus.ifaaservice
pm uninstall --user 0 com.oneplus.filemanager
pm uninstall --user 0 com.oneplus.filemanager.black.overlay
pm uninstall --user 0 com.oneplus.filemanager.white.overlay
pm uninstall --user 0 com.oneplus.gallery
pm uninstall --user 0 com.oneplus.gamespace
pm uninstall --user 0 com.oneplus.gamespace.black.overlay
pm uninstall --user 0 com.oneplus.gamespace.white.overlay
pm uninstall --user 0 com.oneplus.mms
pm uninstall --user 0 com.oneplus.mms.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.mms.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.note.black.overlay
pm uninstall --user 0 com.oneplus.note.white.overlay
pm uninstall --user 0 com.oneplus.opbackup
pm uninstall --user 0 com.oneplus.opbackup.black.overlay
pm uninstall --user 0 com.oneplus.opbackup.white.overlay
pm uninstall --user 0 com.oneplus.opbugreportlite
pm uninstall --user 0 com.oneplus.opsports.black.overlay
pm uninstall --user 0 com.oneplus.opsports.white.overlay
pm uninstall --user 0 com.oneplus.opwlb.black.overlay
pm uninstall --user 0 com.oneplus.opwlb.white.overlay
pm uninstall --user 0 com.oneplus.overlay
pm uninstall --user 0 com.oneplus.screenrecord
pm uninstall --user 0 com.oneplus.screenrecord.black.overlay
pm uninstall --user 0 com.oneplus.screenrecord.white.overlay
pm uninstall --user 0 com.oneplus.twspods
pm uninstall --user 0 net.oneplus.commonlogtool
pm uninstall --user 0 net.oneplus.launcher  ## needed for Gesture like home / recent app
pm uninstall --user 0 net.oneplus.launcher.black.overlay
pm uninstall --user 0 net.oneplus.launcher.white.overlay
pm uninstall --user 0 net.oneplus.odm
pm uninstall --user 0 net.oneplus.odm.provider
pm uninstall --user 0 net.oneplus.provider.appcategoryprovider
pm uninstall --user 0 net.oneplus.push
pm uninstall --user 0 net.oneplus.weather.basiccolorblack.overlay
pm uninstall --user 0 net.oneplus.weather.basiccolorwhite.overlay
pm uninstall --user 0 com.oem.autotest
pm uninstall --user 0 com.oem.logkitsdservice
pm uninstall --user 0 com.oem.nfc
pm uninstall --user 0 com.oem.oemlogkit
pm uninstall --user 0 com.oem.rftoolkit
pm uninstall --user 0 com.oneplus.account
pm uninstall --user 0 com.oneplus.account.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.account.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.brickmode
pm uninstall --user 0 com.oneplus.bttestmode
pm uninstall --user 0 com.oneplus.calculator
pm uninstall --user 0 com.oneplus.calculator.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.calendar.black.overlay
pm uninstall --user 0 com.oneplus.calendar.white.overlay
pm uninstall --user 0 com.oneplus.camera
pm uninstall --user 0 com.oneplus.camera.resources
pm uninstall --user 0 com.oneplus.camera.service
pm uninstall --user 0 com.oneplus.card.black.overlay
pm uninstall --user 0 com.oneplus.card.white.overlay
pm uninstall --user 0 com.oneplus.cloud.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.cloud.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.contacts
pm uninstall --user 0 com.oneplus.contacts.basiccolorblack.overlay
pm uninstall --user 0 com.oneplus.contacts.basiccolorwhite.overlay
pm uninstall --user 0 com.oneplus.ses
pm uninstall --user 0 com.google.android.apps.docs
pm uninstall --user 0 com.google.android.apps.photos
pm uninstall --user 0 com.google.android.apps.restore
pm uninstall --user 0 com.google.android.apps.tachyon
pm uninstall --user 0 com.google.android.apps.turbo
pm uninstall --user 0 com.google.android.as
# pm uninstall --user 0 com.google.android.documentsui ## needed for file API
pm uninstall --user 0 com.google.android.feedback
pm uninstall --user 0 com.google.android.gms.location.history
pm uninstall --user 0 com.google.android.googlequicksearchbox
pm uninstall --user 0 com.google.android.marvin.talkback
pm uninstall --user 0 com.google.android.modulemetadata
pm uninstall --user 0 com.google.android.music
pm uninstall --user 0 com.google.android.printservice.recommendation
pm uninstall --user 0 com.google.android.youtube
pm uninstall --user 0 com.google.android.videos
pm uninstall --user 0 com.google.ar.core
pm uninstall --user 0 com.recognize.number
```
