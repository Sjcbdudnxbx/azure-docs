---
title: Azure Active Directory SSO integration with courses.work
description: Learn how to configure single sign-on between Azure Active Directory and courses.work.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: how-to
ms.date: 02/16/2023
ms.author: jeedes

---

# Azure Active Directory SSO integration with courses.work

In this article, you learn how to integrate courses.work with Azure Active Directory (Azure AD). courses.work is a product of Succeed Technologies®, a ISO 27001-2013 company with rich experience in developing engaging and interactive eLearning. When you integrate courses.work with Azure AD, you can:

* Control in Azure AD who has access to courses.work.
* Enable your users to be automatically signed-in to courses.work with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

You'll configure and test Azure AD single sign-on for courses.work in a test environment. courses.work supports **IDP** initiated single sign-on and **Just In Time** user provisioning.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Prerequisites

To integrate Azure Active Directory with courses.work, you need:

* An Azure AD user account. If you don't already have one, you can [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* One of the following roles: Global Administrator, Cloud Application Administrator, Application Administrator, or owner of the service principal.
* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* courses.work single sign-on (SSO) enabled subscription.

## Add application and assign a test user

Before you begin the process of configuring single sign-on, you need to add the courses.work application from the Azure AD gallery. You need a test user account to assign to the application and test the single sign-on configuration.

### Add courses.work from the Azure AD gallery

Add courses.work from the Azure AD application gallery to configure single sign-on with courses.work. For more information on how to add application from the gallery, see the [Quickstart: Add application from the gallery](../manage-apps/add-application-portal.md).

### Create and assign Azure AD test user

Follow the guidelines in the [create and assign a user account](../manage-apps/add-application-portal-assign-users.md) article to create a test user account in the Azure portal called B.Simon.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, and assign roles. The wizard also provides a link to the single sign-on configuration pane in the Azure portal. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides). 

## Configure Azure AD SSO

Complete the following steps to enable Azure AD single sign-on in the Azure portal.

1. In the Azure portal, on the **courses.work** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, the user does not have to perform any step as the app is already pre-integrated with Azure.

1. courses.work application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![Screenshot shows the image of attributes configuration.](common/default-attributes.png "Image")

1. In addition to above, courses.work application expects few more attributes to be passed back in SAML response, which are shown below. These attributes are also pre populated but you can review them as per your requirements.

	| Name |  Source Attribute|
	| ---------------|  --------- |
    | email | user.mail |
	| firstname | user.givenname |
	| lastname | user.surname |
	| username | user.userprincipalname |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section, click copy button to copy **App Federation Metadata Url** and save it on your computer.

	![Screenshot shows the Certificate download link.](common/copy-metadataurl.png "Certificate")

## Configure courses.work SSO

To configure single sign-on on **courses.work** side, you need to send the **App Federation Metadata Url** to [courses.work support team](mailto:support@succeedtech.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create courses.work test user

In this section, a user called B.Simon is created in courses.work. courses.work supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in courses.work, a new one is created after authentication.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options.

* Click on Test this application in Azure portal and you should be automatically signed in to the courses.work for which you set up the SSO.

* You can use Microsoft My Apps. When you click the courses.work tile in the My Apps, you should be automatically signed in to the courses.work for which you set up the SSO. For more information, see [Azure AD My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Additional resources

* [What is single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
* [Plan a single sign-on deployment](../manage-apps/plan-sso-deployment.md).

## Next steps

Once you configure courses.work you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).