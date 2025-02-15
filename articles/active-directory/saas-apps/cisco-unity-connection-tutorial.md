---
title: Azure Active Directory SSO integration with Cisco Unity Connection
description: Learn how to configure single sign-on between Azure Active Directory and Cisco Unity Connection.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: how-to
ms.date: 05/05/2023
ms.author: jeedes

---

# Azure Active Directory SSO integration with Cisco Unity Connection

In this article, you learn how to integrate Cisco Unity Connection with Azure Active Directory (Azure AD). Cisco Unity Connection is a robust unified messaging and voicemail solution that provides users with flexible message access options including support for voice commands, STT transcriptions etc. When you integrate Cisco Unity Connection with Azure AD, you can:

* Control in Azure AD who has access to Cisco Unity Connection.
* Enable your users to be automatically signed-in to Cisco Unity Connection with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

You configure and test Azure AD single sign-on for Cisco Unity Connection in a test environment. Cisco Unity Connection supports **SP** initiated single sign-on.

## Prerequisites

To integrate Azure Active Directory with Cisco Unity Connection, you need:

* An Azure AD user account. If you don't already have one, you can [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* One of the following roles: Global Administrator, Cloud Application Administrator, Application Administrator, or owner of the service principal.
* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Cisco Unity Connection single sign-on (SSO) enabled subscription.

## Add application and assign a test user

Before you begin the process of configuring single sign-on, you need to add the Cisco Unity Connection application from the Azure AD gallery. You need a test user account to assign to the application and test the single sign-on configuration.

### Add Cisco Unity Connection from the Azure AD gallery

Add Cisco Unity Connection from the Azure AD application gallery to configure single sign-on with Cisco Unity Connection. For more information on how to add application from the gallery, see the [Quickstart: Add application from the gallery](../manage-apps/add-application-portal.md).

### Create and assign Azure AD test user

Follow the guidelines in the [create and assign a user account](../manage-apps/add-application-portal-assign-users.md) article to create a test user account in the Azure portal called B.Simon.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, and assign roles. The wizard also provides a link to the single sign-on configuration pane in the Azure portal. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides). 

## Configure Azure AD SSO

Complete the following steps to enable Azure AD single sign-on in the Azure portal.

1. In the Azure portal, on the **Cisco Unity Connection** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, if you have **Service Provider metadata file** then perform the following steps:

	a. Click **Upload metadata file**.

    ![Screenshot shows how to upload metadata file.](common/upload-metadata.png "File")

	b. Click on **folder logo** to select the metadata file and click **Upload**.

	![Screenshot shows to choose and browse metadata file.](common/browse-upload-metadata.png "Folder")

	c. After the metadata file is successfully uploaded, the **Identifier** and **Reply URL** values get auto populated in Basic SAML Configuration section.

	d. In the **Sign on URL** textbox, type a URL using the following pattern:
	`https://<FQDN_CUC_node>`

	> [!Note]
	> You will get the **Service Provider metadata file** from the [Cisco Unity Connection support team](mailto:unity-tme@cisco.com). If the **Identifier** and **Reply URL** values do not get auto populated, then fill the values manually according to your requirement.

1. Cisco Unity Connection application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![Screenshot shows the image of attributes configuration.](common/default-attributes.png "Image")

1. In addition to above, Cisco Unity Connection application expects few more attributes to be passed back in SAML response which are shown below. These attributes are also pre populated but you can review them as per your requirements.

	| Name |  Source Attribute|
	| ---------------|  --------- |
	| uid | user.onpremisessamaccountname |

1. On the **Set-up single sign-on with SAML** page, in the **SAML Signing Certificate** section, find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

    ![Screenshot shows the Certificate download link.](common/metadataxml.png "Certificate")

1. On the **Set up Cisco Unity Connection** section, copy the appropriate URL(s) based on your requirement.

	![Screenshot shows how to copy configuration appropriate URL.](common/copy-configuration-urls.png "Metadata")

## Configure Cisco Unity Connection SSO

To configure single sign-on on **Cisco Unity Connection** side, you need to send the downloaded **Federation Metadata XML** and appropriate copied URLs from Azure portal to [Cisco Unity Connection support team](mailto:unity-tme@cisco.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create Cisco Unity Connection test user

In this section, you create a user called Britta Simon in Cisco Unity Connection. Work with [Cisco Unity Connection support team](mailto:unity-tme@cisco.com) to add the users in the Cisco Unity Connection platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

* Click on **Test this application** in Azure portal. This will redirect to Cisco Unity Connection Sign-on URL where you can initiate the login flow. 

* Go to Cisco Unity Connection Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you click the Cisco Unity Connection tile in the My Apps, this will redirect to Cisco Unity Connection Sign-on URL. For more information, see [Azure AD My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Additional resources

* [What is single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
* [Plan a single sign-on deployment](../manage-apps/plan-sso-deployment.md).

## Next steps

Once you configure Cisco Unity Connection you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).