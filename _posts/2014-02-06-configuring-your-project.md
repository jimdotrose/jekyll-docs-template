---
layout: page
title: "Configuring your Project"
category: doc
date: 2014-02-06 13:23:14
---

Before Distiller can build your iOS app, you'll need to specify the settings of your project.

#####1.Select your Project or Workspace

You need to define the app path for Distiller to build.  Distiller can build either independent `.xcodeproj` project or shared `.xcworkspace` workspace. Identify the target of the build, and then enter into your settings.  This should be the repo-relative path to the `.xcodeproj` or `.xcworkspace` file.  Example would be `Distiller/Distiller.xcworkspace`.
<br />
<br />

#####2. Add the Scheme

This should be the scheme you'd like Distiller to use to build your app. Important - this scheme must be shared.  You change this settings in Xcode at Product > Scheme > Manage Schemes and you'll see the share settings.

![Xcode Scheme Settings](/jekyll-docs-template/img/xcode-scheme-settings.png)