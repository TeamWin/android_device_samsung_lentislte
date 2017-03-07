## TWRP device tree for Galaxy S5 Plus (International)

Add to `.repo/local_manifests/lentislte.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project path="device/samsung/lentislte"
	   name="github-cygwin/twrp_android_device_samsung_lentislte"
	   remote="github"
	   revision="android-7.1" />
  <project name="LineageOS/android_vendor_qcom_opensource_cryptfs_hw"
	   path="vendor/qcom/opensource/cryptfs_hw"
	   remote="github"
	   revision="cm-14.1" />
  <project path="kernel/samsung/apq8084"
	   name="github-cygwin/android_kernel_samsung_apq8084"
	   remote="github"
	   revision="cm-14.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_lentislte-eng
mka recoveryimage
```
