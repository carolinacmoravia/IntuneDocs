---
# required metadata

title: Set terms and conditions in Microsoft IntunetitleSuffix: "Intune Azure preview"
description: "Set terms and conditions that users see in the Company Portal for Intune. "
keywords:
author: nathbarn
ms.author: nathbarn
manager: angrobe
ms.date: 05/05/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 4a3a11a8-9c0c-4334-8c6b-6fea4d0a2efb

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: amyro
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure
---

# Ensure users accept company terms for access

[!INCLUDE[azure_preview](../includes/azure_preview.md)]

As an Intune admin, you can choose to require that users accept your company's terms and conditions before they can use the Company Portal to enroll their devices and access company resources like apps and email. Configuration of terms and conditions is optional.

You can create multiple sets of terms and assign them to different groups, such as to support different languages.

## Create terms and conditions
Complete these steps to create terms and conditions. The display name and description are for administrative use while terms properties are displayed to users in the Company Portal.

1. In the Azure portal, choose **More Services** > **Monitoring + Management** > **Intune**.

2. On the Intune blade, choose **Device enrollment**, and then choose **Terms and Conditions**.

3. Select **Create**.
![Screenshot of the Intune portal showing Create button for terms and conditions](media/terms-create-terms.png)

4. On the expanded blade, specify the following information:

   - **Display name**: The name for the terms in the Intune portal. Users don't see this name.

   - **Description**: Optional details that help you identify this set of terms in the Intune portal.

5. Select the arrow next to Define terms of use to open the Terms and Conditions blade, and then enter the following information:

   ![Screenshot of end user terms and conditions acceptance screen with summary of terms](../media/terms-summary-create.png)

   - **Title**: The title that users see in the Company Portal.

   - **Summary of Terms**: Text that explains what it means if users accept the terms. Eg "By enrolling your device, you are agreeing to the terms of use set out by Contoso. Read the terms carefully before proceeding."

   - **Terms and Conditions**: The terms and conditions that users see and must either accept or reject.

6. Select **Ok** and then select **Create**.

## Assign terms and conditions

You can assign terms and conditions to groups of user who must accept them before using the Company Portal.

1. In the Azure portal, choose **More Services** > **Monitoring + Management** > **Intune**.

2. On the Intune blade, choose **Device enrollment**, and then choose **Terms and Conditions**.

3. In the list of terms and conditions, select the terms you want to assign, and then select **Assigned Groups**.
![Screenshot of the Intune portal's Assign Group blade showing Select Group button and Select button for terms and conditions assignment](media/terms-assign-groups.png)

4. Click the **Select Group** button and in the **Select Groups** blade, select the groups you want to assign the terms, and then click **Select**.

5. In the **Assigned Groups** blade, click **Save**.  The terms and conditions are now assigned to users in the selected groups. Users will be prompted to accept terms the next time they access the company portal.

   ![Screenshot of end user terms and conditions acceptance screen with summary of terms](../media/terms-summary-accept.png)

## Monitor a terms and conditions

1. In the Azure portal, choose **More Services** > **Monitoring + Management** > **Intune**. On the Intune blade, choose **Device enrollment**, and then choose **Terms and Conditions**.
2. In the list of terms and conditions, select the terms you want to view acceptance for, and then select **Acceptance Statuses**.

## Work with multiple versions of terms and conditions
You can edit your terms and conditions and manage their versions. We recommend that you increase the version number and require acceptance any time you make significant changes to your terms and conditions. Keep the current version number if, for example, you are fixing typos or changing formatting.

1. In the Azure portal, choose **More Services** > **Monitoring + Management** > **Intune**.

2. On the Intune blade, choose **Device enrollment**,  choose **Terms and Conditions**, select the terms and conditions you want to modify, and then select **Properties**.

4. On the **Properties** blade, select **Terms and Conditions** and then modify the **Title**, **Summary of Terms**, and **Terms and Conditions** as needed. If the changes you made make it necessary for users to re-accept the new terms, click **Require users to re-accept, and increment the version number to**

4.  Select **OK** and then select **Save**.
