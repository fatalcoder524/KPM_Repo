# Critical_Partitions_Protect
Critical Partitions Protect is a KPM used to protect your partitions from harmful apps and modules which try to modify and format system partitions by @GarfieldHan.
After loading it, any malicious operation will fail. It directly blocks access at the kernel level and returns a "no permission" error, even if you have ROOT privileges.

Follow the authors and support them at: https://github.com/pomelohan and https://github.com/sekaiacg

KPMs are normally released in TG Group:https://t.me/apatch_discuss

Original Source: https://github.com/AndroidPatch/kpm

All Rights belong to the original developers! I'm just keeping this for my personal use or quick indexing and sharing. 

## Note:
- Before performing system OTA or software updates, you can temporarily disable the protection by clicking the "Unload" button in the KPM interface. After the system restarts, the protection will be automatically reloaded.
- After downloading the KPM, please first click "Load" in the KPM interface to test it. If it loads successfully without a restart, you can then "embed" it into the kernel. Otherwise, the device will fail to boot.
- ⚠️Don't use this KPM, if your kernel already has [Baseband Guard (BBG)](https://github.com/vc-teahouse/Baseband-guard) Support.⚠️

# Changelogs

## critical_partition_protect_1.1.kpm
- critical_partition_protect: Fix wrong branch predict
