---
# required metadata

title: Deploy Lookout for Work app | Microsoft Intune
description: Configure and deploy Lookout for Work apps for Android.
author: karthikaraman
manager: angrobe
ms.date: 09/13/2016
ms.topic: article
ms.prod:
ms.service:
ms.technology:
ms.assetid: 524c4209-ad57-4d35-955e-a00d796bf858

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: sandera
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Configure and deploy Lookout for Work apps
This article explains how to configure and deploy the Lookout for Work app for devices that are enrolled and that are running Android 4.1 or later.

* **Step 1:**	In the [Microsoft Intune administrator console](https://manage.microsoft.com), go to **Apps** and choose **Add Apps**.   
* **Step 2:**	On the **Software Setup** page of the publisher, choose **External link**, and specify the following URL:  https://play.google.com/store/apps/details?id=com.lookout.enterprise
>[!NOTE]
>Do not click the box for requiring a managed browser.

* **Step 3:**	On the **Software description** page fill in the following information:
  * **Publisher:** Lookout Mobile Security
  * **Name:**   Lookout for Work
  * **Description:**  Lookout offers the best protection against mobile threats to keep your device safe. When the Lookout app is installed on the device, the app protects your device from threats and will alert you and your company administrator, if any are found.
  * **Category:** Computer Management
* **Step 4:**  Upon successful completion you see a message **Upload of data to Microsoft Intune successfully completed**.

When you click  **Apps** in the Intune administrator console, you now see the Lookout for Work app in the list
![screenshot of Intune admin console apps page showing the Lookout for work apps in the list](../media/mtp/lookout-app-listed-intune-console.png)

**To deploy the app to users**, select the Lookout for Work app shown in the screen above and select **Manage Deployment**.

You must select the same users that were added to the Enrollment Management option in the Lookout  console.  See Step 3 in the [configure your subscription with Lookout device threat protection section](set-up-your-subscription-with-lookout-mtp#configure-your-subscription-with-lookout-mtp) for information about adding user groups to Lookout MTP.
>[!IMPORTANT]
> The Intune app deployment wizard is not aware of the Azure AD user groups and uses the Intune user groups instead, so you must create an Intune user group based on the Azure AD user group that is enrolled in the Lookout console as described in [this](plan-your-user-and-device-groups.md) topic.

Choose the **Required Install** option to require that the Lookout app be installed on the user’s device.


With the **Required Install** option selected for deployment, Intune will push the Lookout for work application to the device.   

When the user opens the Lookout for Work on the device they are prompted to activate the app, and choose the Sign in with Azure Active Directory option. A detailed walkthrough with the end-user flow can be found in the following topics:

* [You are prompted to install Lookout for Work on your Android device](http://docs.microsoft.com/intune/enduser/you-are-prompted-to-install-lookout-for-work-android)

* [You need to resolve a threat that Lookout for Work found on your Android device](http://docs.microsoft.com/intune/enduser/you-need-to-resolve-a-threat-found-by-lookout-for-work-android)

## Next steps
* [Enable device threat protection rule in the compliance policy](enable-device-threat-protection-rule-in-compliance-policy.md)
