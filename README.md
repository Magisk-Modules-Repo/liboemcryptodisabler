# liboemcrypto.so disabler

## Description

Apps that use `liboemcrypto.so` for DRM, such as Netflix and My5, will fail during playback on rooted devices. This Magisk module masks `liboemcrypto.so` with a zero byte replacement.

## Changelog

2018-04-23: v1

## Requirements
- The module assumes the library is located at `/system/lib/liboemcrypto.so`. If your library is located elsewhere (or nowhere), the module will have no effect.

- The module has been verified working on a Samsung Galaxy S9+ (SM-G965F/DS) running Magisk 16.3 installed by v1.9 of SoLdieR9312's Stock ROM.
