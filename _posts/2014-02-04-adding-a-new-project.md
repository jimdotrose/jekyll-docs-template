---
layout: page
title: "Setting Up Your First Project"
category: doc
date: 2014-02-04 12:52:15
---


### #1: Setting up your Distiller Project with Apple#

This guide is designed to get your Apple Certificates and Provisioning Profiles set up for your first Distiller project. Getting an iOS project set up with Apple can be a pretty involved process. We will walk through all the necessary steps to get your Apple account set up to build your first Distiller project.


**IMPORTANT - Open a Safari browser (if you have it available) for the steps involving Apple. While other browsers can work, there's no guarantee. Safari will for sure work so you can save yourself some frustration.**
<br />
<br />

#####1. Add a New Project#

Get started by clicking "Add a New Project" on the Distiller site.
<br />
<br />

#####2. Download your Distiller CSR

To build your iOS project, Distiller needs to be able to sign your code for you. To do that, you'll need to generate a new Apple Certificate.  Click the "Download CSR" button on the Distiller page and your Distiller CSR ("distiller.certSigningRequest") will download to your machine. Keep that file handy.
<br />
<br />

#####3. Log into your Apple Developer account and get to your Certificate List

Go to https://developer.apple.com, log in, and navigate to "Certificates, Identifiers & Profiles".

![Apple Developer Home](/jekyll-docs-template/img/01-dev-center-home.png?raw=true) 

<br />
Select "Certificates" to navigate to your iOS Certificate List.


![Apple Certificates](/jekyll-docs-template/img/02-select-certificates.png)
<br />
<br />

#####4. Create a New Certificate

You should be viewing your list of iOS Certificates. We need to create a new one for your Distiller builds. Click on the "+" to enter the "Add iOS Certificate" flow.

![iOS Certificate List](/img/03-add-new-certificate.png)
<br />
<br />

#####5. Select the Certificate Type

Now, you have to select your certificate type. Select "App Store and Ad Hoc" for the type of certificate you wish to create and click "Continue."

![iOS Certificate Type](/img/04-select-certificate-type.png)
<br />
<br />

*IGNORE THIS NEXT PAGE. You can ignore the description of generating a CSR. We've already generated a CSR with the Distiller details for you. Just click "Continue".*
<br />
<br />

#####6. Upload your Distiller CSR

You should now see a file selector to select the CSR for your new certificate.

![iOS CSR Selection](/img/05-upload-csr.png)
<br />
<br />

Select the file that you downloaded from Distiller ("distiller.certSigningRequest") and then click "Generate."

DONE. Your new Apple Certificate has been generated.  You can choose to download it if you choose, but it's not necessary to set up your Distiller project.
<br />
<br />

#####7. Create a new Provisioning Profile

Now, we need to create a new Provisioning Profile for your Distiller project.  A Provisioning Profile defines who can install and use your unreleased iOS app (developers, testers, etc).

Click "Provisioning Profiles > All" on the left nav.

![Go To Provisioning Profiles](/img/06-goto-provisioning-profiles.png)
<br />
<br />

You should see a list of all of your provisioning profiles. Click the "+" to generate a new profile.  

![Add Provisioning Profile](/img/07-add-provisioning-profile.png)
<br />
<br />

#####8. Select the Provisioning Profile Type

You should see the Select Profile Type page. Select "Ad Hoc" as the provisioning profile type and click "Continue."

![Select Provisioning Profile Type](/img/08-select-profile-type.png)
<br />
<br />
￼
#####9. Select the App ID for the Provisioning Profile

Select the app id of the project you are building on Distiller, then click "Continue."

![Select iOS App ID](/img/09-select-app-id.png)
<br />
<br />

#####10. Select the Certificate for the Provisioning Profile.

Now, associate this Provisioning Profile with your new Certificate. Select the certificate that you just created. In some cases, you may have more than one with the same name, and you will have to use the expiry date to find the right one. It will be 1 year from the day it was created (likely today). Click "Continue."

![Select Certificate](/img/10-select-certificate.png)
<br />
<br />
￼
#####11. Select the devices for the Provisioning Profile

Now, you can select what devices will be able to download and install the app. Select the devices from your device list and click "Continue."

![Select Devices](/img/11-select-devices.png)
<br />
<br />
￼
#####12. Name and generate the Provisioning Profle

You're now ready to save the Provisioning Profile. Enter "distiller" as the profile name and click "Generate."

![Name Provisioning Profile](/img/12-name-save-provisioning-profile.png)
<br />
<br />
￼
#####13. Download your Provisioning Profile.
Download the new Provisioning Profile you just created to your machine, which will be named "distiller.mobileprovision".  Keep that handy.

![Download Provisioning Profile](/img/13-download-provisioning-profile.png)
<br />
<br />

#####14. Add your Provisioning Profile to your Git Repository
On your machine, locate your iOS project that you're adding to Distiller.  From the root directory, find the /profiles folder (create one if it does not exist). Take the provisioning profile document and add it to your /profiles folder. 

Now, commit your change and sync this repo with GitHub.  This will trigger a new build with Distiller (which will fail - don't worry - you're project isn't configured yet). 

Now, we are ready to configure your Xcode project settings.  
