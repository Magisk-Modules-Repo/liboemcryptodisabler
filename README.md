# **liboemcrypto.so disabler**

## Description

Apps that use `liboemcrypto.so` to play content protected by DRM, such as Netflix and My5, will fail when playback is attempted on a rooted device. This Magisk module masks `liboemcrypto.so` with a zero byte replacement.

## FAQ

Q. Can't I just delete or rename `liboemcrypto.so` to achieve the same effect?

A. You can, but then you will have a modified `/system` partition. The beauty of using a Magisk module is that no actual changes are made to your file system.

## Problems

A consequence of using this module is that Widevine DRM will fall back to using L3 instead of L1, which means that Netflix will not display content in HD or higher quality, regardless of your subscription type. Of course, without this module, Netflix will not play **at all** on a rooted device. If this is important to you, you will need to unroot your device.

## Changelog

2018-07-22: v1.2

- Add logic to install only to the library directory actually used by the device, rather than installing to both commonly used directories.

2018-05-29: v1.1

- Add support for devices that have the library under `/system/vendor/lib` instead of `/system/lib`.

2018-04-23: v1.0

- Initial release.

## Requirements
- The module assumes the library in question is located at either `/system/lib/liboemcrypto.so` or `/system/vendor/lib/liboemcrypto.so`. If your library is located elsewhere (or nowhere), the module will have no effect (so it's harmless to try it).

- The module has been verified working on a Samsung Galaxy S9+ (SM-G965F/DS) running Magisk 16.x/17.x on a variery of ROMs, on a Samsung Tab S3 (SM-T820) running stock Android 8.0 and Magisk 16.x/17.x, and on a Samsung Tab S4 (SM-T830) running stock Android 8.1 and Magisk 17.x.

## Links
[Module's XDA forum thread](https://forum.xda-developers.com/apps/magisk/magisk-liboemcrypto-disabler-drm-t3794393)
