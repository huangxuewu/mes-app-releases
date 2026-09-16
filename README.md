# MES Store

Android apps for the MES workplace. This repository hosts public APK downloads and the MES Store catalog. Application source code remains in separate private repositories.

## Install MES Store

Download [MES Store 1.2.0](https://github.com/huangxuewu/mes-app-releases/releases/download/mes-store-v1.2.0/mes-store-1.2.0.apk) on your Android phone and open the APK. Android 9 or newer is required.

Use **Featured** to discover apps and **Apps** to browse the full catalog. Tap an app to open its download page. **Tutorial** contains step-by-step guides with illustrated PDFs and offline reading. **Settings** controls automatic update checks, optional automatic downloads, and connection preferences. The first time you install an app through the store, Android will ask you to enable **Allow from this source** for MES Store. Downloads are public; MES authorization is still required to access company services and data.

## Tutorials

**How to use SignPad** covers picking, labeling, inspection, loading, shipper and driver signatures, and printing the signed BOL. Open Tutorial in MES Store, or download the [11-page illustrated guide](https://github.com/huangxuewu/mes-app-releases/releases/download/tutorial-signpad-daily-workflow-v1/signpad-daily-workflow.pdf). The examples use training data; always scan your current paperwork.

`tutorials.json` contains the article content, page links, and PDF integrity metadata. The store saves each verified PDF for offline reading after its first download.

## Updates

Open the store or tap **Refresh** in Apps, choose an app, and finish your current work before tapping **Install now**. Automatic checks run about once a day when enabled. Optional automatic downloads prepare installed-app updates; they do not install silently. Android asks for installation approval. Updating an app in place preserves its data. Do not uninstall SignPad to work around a signing-certificate mismatch; contact your administrator.

The store checks APK checksums, package identity, version, and signing certificates before installation. Each release includes an APK and SHA-256 checksum. `catalog.json` lists the currently offered version of each app, including MES Store itself.

Only complete, signed APKs are published. No company data, credentials, or signing keys belong in this repository.
