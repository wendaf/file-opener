<p align="center"><br><img src="https://user-images.githubusercontent.com/236501/85893648-1c92e880-b7a8-11ea-926d-95355b8175c7.png" width="128" height="128" /></p>
<h3 align="center">File Opener</h3>
<p align="center"><strong><code>@capacitor-community/file-opener</code></strong></p>
<p align="center">
  Capacitor File Opener. The plugin is able to open a file given the mimeType and the file uri.
</p>

<p align="center">
  <img src="https://img.shields.io/maintenance/yes/2022?style=flat-square" />
  <a href="https://www.npmjs.com/package/@capacitor-community/file-opener"><img src="https://img.shields.io/npm/l/@capacitor-community/file-opener?style=flat-square" /></a>
<br>
  <a href="https://www.npmjs.com/package/@capacitor-community/file-opener"><img src="https://img.shields.io/npm/dw/@capacitor-community/file-opener?style=flat-square" /></a>
  <a href="https://www.npmjs.com/package/@capacitor-community/file-opener"><img src="https://img.shields.io/npm/v/@capacitor-community/file-opener?style=flat-square" /></a>
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<a href="#contributors-"><img src="https://img.shields.io/badge/all%20contributors-1-orange?style=flat-square" /></a>
<!-- ALL-CONTRIBUTORS-BADGE:END -->
</p>

## Table of Contents

- [Maintainers](#maintainers)
- [About](#about)
- [Installation](#installation)
- [API](#api)
- [Troubleshooting](#troubleshooting)

## Maintainers

| Maintainer | GitHub                                | Active |
| ---------- | ------------------------------------- | ------ |
| ryaa       | [ryaa](https://github.com/ryaa)       | yes    |


## About

This plugin is similar to cordova-plugin-file-opener2 but without installation support. The plugin supports Android platform only.

## Installation

```bash
npm install @capacitor-community/file-opener
npx cap sync
```

## API

<docgen-index>

* [`open(...)`](#open)
* [Interfaces](#interfaces)

</docgen-index>

<docgen-api>
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

### open(...)

```typescript
open(options: FileOpenerOptions) => Promise<void>
```

Method to open a file.

| Param         | Type                                                            |
| ------------- | --------------------------------------------------------------- |
| **`options`** | <code><a href="#fileopeneroptions">FileOpenerOptions</a></code> |

**Since:** 1.0.0

--------------------


### Interfaces


#### FileOpenerOptions

file open method options

| Prop                  | Type                 | Description                                                                                                                                                                                                                                                                                                                                                                            | Since |
| --------------------- | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| **`filePath`**        | <code>string</code>  | file path                                                                                                                                                                                                                                                                                                                                                                              | 1.0.0 |
| **`contentType`**     | <code>string</code>  | MIME type                                                                                                                                                                                                                                                                                                                                                                              | 1.0.0 |
| **`openWithDefault`** | <code>boolean</code> | Use the default Android platform chooser. If false, it will show "Open File in.." title of the chooser dialog, the system will always present the chooser dialog even if the user has chosen a default one and if no activity is found to handle the file, the system will still present a dialog with the specified title and an error message No application can perform this action | 1.0.0 |

</docgen-api>

### Android

If you app needs to open files in the external directories, then within your `AndroidManifest.xml` file, change the following:

```diff
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android" package="com.example">

+  <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />

</manifest>
```