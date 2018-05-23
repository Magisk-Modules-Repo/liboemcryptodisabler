# **liboemcrypto.so disabler**

## Description

Apps that use `liboemcrypto.so` to play content protected by DRM, such as Netflix and My5, will fail when playback is attempted on a rooted device. This Magisk module masks `liboemcrypto.so` with a zero byte replacement.

## FAQ

Q. Can't I just delete or rename `liboemcrypto.so` to achieve the same effect?

A. You can, but then you will have a modified `/system` partition. The beauty of using a Magisk module is that no actual changes are made to your file system.

## Changelog

2018-04-23: v1

## Requirements
- The module assumes the library in question is located at `/system/lib/liboemcrypto.so`. If your library is located elsewhere (or nowhere), the module will have no effect (so it's harmless to try it).

- The module has been verified working on a Samsung Galaxy S9+ (SM-G965F/DS) running Magisk 16.x on a variery of ROMs.

## Links
[Module's XDA forum thread](https://forum.xda-developers.com/apps/magisk/magisk-liboemcrypto-disabler-drm-t3794393)
