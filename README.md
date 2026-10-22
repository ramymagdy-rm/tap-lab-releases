# Tap Lab Emulator — releases

The Tap Lab Emulator is a small Android app that lets your phone
present one of your saved Tap Lab tags to a reader, as an NFC tag. You
pick the tag in the Tap Lab web app (<https://tap-lab.web.app>) and tap
**Emulate on this phone**; the Emulator opens and holds it.

This repo only holds the signed APK, until the app is on Google Play.
The source is private; releases are made by its CI.

## What it does and does not do

- It presents the tag's **NDEF content** (a URL, text, a contact…) as
  an NFC Forum Type 4 tag, using Android's host card emulation.
- It does **not** copy a tag's UID: Android gives an emulated tag a
  random one. Door badges, transit cards and payment cards cannot be
  emulated, and Tap Lab never tries.
- It has no account and asks for **no internet permission**.

## Install (Android 8 or later, with NFC)

1. On the phone, open the latest release and download
   `TapLabEmulator.apk`, or use **Get the app** in the web app.
2. Open the file. Android asks to allow installs from your browser
   once: allow it, then **Install**.
3. Optionally, check the file first: `SHA256SUMS` in the same release
   lists its SHA-256.

Updates install over the old version: they are signed with the same
key.
