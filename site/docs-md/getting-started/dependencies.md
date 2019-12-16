---
title: Capacitor Required Dependencies
description: Required Dependencies for different platforms
url: /docs/getting-started/dependencies
contributors:
  - mlynch
  - dotnetkow
---

# Capacitor Required Dependencies

<p class="intro">Capacitor has a number of dependencies depending on which platforms you're targeting and which operating systems you are developing on.</p>

## Requirements

The base requirements are **[Node v8.6.0](https://nodejs.org) or later**, and **NPM version 5.6.0 or later** (which is usually automatically installed with the required version of Node).

Capacitor supports [yarn](https://yarnpkg.com) as well.

For specific platforms, follow each guide below to ensure you have the correct dependencies installed.

## iOS Development

For building iOS apps, Capacitor requires a **Mac with Xcode 10 or above**. Soon, you'll be able to use [Ionic Appflow](http://ionicframework.com/appflow) to build for iOS even if you're on Windows.

Additionally, you'll need to install **[CocoaPods](https://cocoapods.org/)** (`sudo gem install cocoapods`), and install the **Xcode Command Line tools** (either from Xcode, or running `xcode-select --install`).

Once you have CocoaPods installed, update your local repo by running `pod repo update`. You should run this command periodically to ensure you have the latest versions of CocoaPods dependencies.

As a rule, the latest version of Capacitor always supports the last two major iOS versions (for example, as of December 2019, iOS 12 and 13). Using the latest version of Capacitor is recommended, though you can use older versions if you need to support older versions of iOS.

Capacitor makes use of `WKWebView` on iOS.

## Android Development

First, the **Java 8 JDK** must be installed and [set to the default](https://stackoverflow.com/a/24657630/32140) if you have other versions of the JDK installed. Java 9 does _not_ work at the moment.

Android development requires the **Android SDK** installed with **[Android Studio](https://developer.android.com/studio/index.html)**. Technically, Android Studio isn't required as you can build and run apps using only the Android CLI tools, but it will make building and running your app much easier so we strongly recommend using it.

Android version support for Capacitor is more complex than iOS. Capacitor currently targets API level 21 or greater, meaning Android 5.0 (Lollipop) or above. [As of May 2019](https://developer.android.com/about/dashboards), this represents over 89% of the Android market.

Capacitor requires an Android WebView with Chrome version 50 or later. On Android 5 and 6, the Capacitor uses the System WebView. On Android 7+, Google Chrome is used.

## Electron Development

As of Capacitor 1.4.0, newly created apps will use Electron version 7.