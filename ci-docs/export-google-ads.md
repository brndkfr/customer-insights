---
title: "Export Customer Insights data to Google Ads"
description: "Learn how to configure the connection and export to Google Ads."
ms.date: 03/31/2022

ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
ms.reviewer: mhart
manager: shellyha
---

# Export segments to Google Ads (preview)

Export segments of unified customer profiles to a Google Ads audience list and use them to advertise on Google Search, Gmail, YouTube, and Google Display Network. 


## Prerequisites for connection

-	You have a [Google Ads account](https://ads.google.com/) and corresponding administrator credentials.
-	You fulfill the requirements of the [Customer Match Policy](https://support.google.com/adspolicy/answer/6299717).
-	You fulfill the requirements of the [remarketing list sizes](https://support.google.com/google-ads/answer/7558048).
-	You have [configured segments](segments.md).
-	Unified customer profiles in the exported segments contain fields representing an email address, phone, mobile advertiser ID, third-party user ID, or address.

## Known limitations

- Exporting to Google Ads is limited to segments.
- Exporting segments with a total of 1 million customer profiles can take up to 30 minutes because of limitations on the provider side. 
- The matching in Google Ads can take up to 48 hours.

## Set up connection to Google Ads

1. Go to **Admin** > **Connections**.

1. Select **Add connection** and choose **Google Ads** to configure the connection.

1. Give your connection a recognizable name in the **Display name** field. The name and the type of the connection describe this connection. We recommend choosing a name that explains the purpose and target of the connection.

1. Choose who can use this connection. If you take no action, the default will be Administrators. For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Enter your **[Google Ads customer ID](https://support.google.com/google-ads/answer/1704344)**.

1. Select **I agree** to confirm the **Data privacy and compliance**.

1. Select **Authenticate with Google Ads** and provide your Google Ads credentials.

1. Select **Add yourself as export user** and provide your Customer Insights credentials.

1. Select **Save** to complete the connection. 

## Configure an export

You can configure this export if you have access to a connection of this type. For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).

1. Go to **Data** > **Exports**.

1. To create a new export, select **Add destination**.

1. In the **Connection for export** field, choose a connection from the Google Ads section. If you don't see this section name, then no connections of this type are available to you.

1. If you want to create a new audience, leave the Google Audience ID field blank. We will automatically create a new audience in your Google Ads account and use the name of the exported segment. If you want to update an existing Google Ads audience, enter your [Google Ads audience ID](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.)

1. In the **Data matching** section, select one or more data fields to export, and select the field that represents the corresponding data fields in Customer Insights.

1. Select the segments you want to export. 

Saving an export doesn't run the export immediately.

The export runs with every [scheduled refresh](system.md#schedule-tab). 

You can also [export data on demand](export-destinations.md#run-exports-on-demand). 

## Data privacy and compliance

When you enable Dynamics 365 Customer Insights to transmit data to Google Ads, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data. Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Google Ads meet any privacy or security obligations you may have. For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).
Your Dynamics 365 Customer Insights administrator can remove this export destination at any time to discontinue use of this functionality.


[!INCLUDE [footer-include](includes/footer-banner.md)]
