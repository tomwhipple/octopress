---
layout: post
title: "Guest post at Testdroid: Using Testdroid Cloud to test a camera SDK"
date: 2012-11-26 07:38
comments: true
categories: Android software programming
---
The great people at [Testdroid](http://testdroid.com) asked me to write a [guest post](http://testdroid.com/testdroid/3524/guest-blog-post-using-testdroid-cloud-to-test-a-camera-sdk) about our experience with their product.

>Developing an SDK that makes heavy use of the camera is different from typical Android app development. First, developing an SDK means that we have to think about ease of integration with other apps. For example, things like XML layouts and ``R.drawable`` are not available to us, since we don't want any unnecessary integration steps. Second, we are doing on-device computer vision, so we have a lot of highly optimized C and even some hand written assembly which must be compiled with the NDK and linked via JNI. And, if you've been fortunate to work with the Android native layer, you know that the toolchain is not quite as stable as the Java SDK. Finally, we're doing frame by frame processing with the camera. Obviously, the camera is a piece of hardware that has been implemented differently by each manufacturer, so there are inevitably some differences in behavior if it is accessed in a way that is not quite as intended.

>[more](http://testdroid.com/testdroid/3524/guest-blog-post-using-testdroid-cloud-to-test-a-camera-sdk)

For small app developers, it is well worth the $100 or so to test on a bunch of different devices, even if you only run the tests once per major release. You'll wish you had done it sooner.