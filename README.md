# zk_finger

A new flutter plugin project.

## Getting Started

This project is a starting point for a Flutter
[plug-in package](https://flutter.dev/developing-packages/),
a specialized package that includes platform-specific implementation code for
Android and/or iOS.

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

#### Add to Android Project:

- In the Manifest permission section add:

 <code>```<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"></uses-permission>
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"></uses-permission>
    <uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED" /> 
    <uses-permission android:name="android.hardware.usb.host" />```</code>
    
    
- Inside the activity tag in the Manifest file add:

<code>```<intent-filter>
    <action android:name="android.hardware.usb.action.USB_DEVICE_ATTACHED" />
    <action android:name="android.intent.action.BOOT_COMPLETED" />
  </intent-filter>
  <meta-data
           android:name="android.hardware.usb.action.USB_DEVICE_ATTACHED"
           android:resource="@xml/device_filter" />```</code>
           
           
- In res folder add xml folder then add *device_filter.xml* with the following content:

<code>```<?xml version="1.0" encoding="utf-8"?>
<resources>
    <usb-device vendor-id="6997" product-id="289" />
</resources>```</code>

Samples:

![alt text](https://github.com/amorenew/flutter_zkteco_fingerprint/raw/master/case1.png)

![alt text](https://github.com/amorenew/flutter_zkteco_fingerprint/raw/master/case2.png)


