---
title: "Enrichment with the third-party enrichment Experian"
description: "General information about the Experian third-party enrichment."
ms.date: 06/10/2022
ms.reviewer: mhart

ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
---

# Enrich customer profiles with demographics from Experian (preview)

Experian is a global leader in consumer and business credit reporting and marketing services. With Experian’s data enrichment services, you can build a deeper understanding of your customers by enriching your customer profiles with demographic data such as household size, income, and more.

## Supported countries/regions

We currently support enriching customer profiles in the United States only.

## Prerequisites

- An active Experian subscription. To get a subscription, [contact Experian](https://www.experian.com/marketing-services/contact) directly. [Learn more about Experian Data Enrichment](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).

- An Experian [connection](connections.md) is [configured](#configure-the-connection-for-experian) by an administrator.

- Experian User ID, Party ID, and Model Number for your SSH-enabled Secure Transport (ST) account that Experian created for you.

## Configure the connection for Experian

You must be an [administrator](permissions.md#admin) in Customer Insights and have an Experian User ID, Party ID, and Model Number.

1. Select **Add connection** when configuring an enrichment, or go to **Admin** > **Connections** and select **Set up** on the Experian tile.

   :::image type="content" source="media/enrichment-Experian-connection.png" alt-text="Experian connection configuration pane.":::

1. Enter a name for the connection and a valid User ID, Party ID, and Model Number for your Experian Secure Transport account.

1. Review and provide your consent for [Data privacy and compliance](#data-privacy-and-compliance) by selecting **I agree**.

1. Select **Verify** to validate the configuration and then select **Save**.

### Data privacy and compliance

When you enable Dynamics 365 Customer Insights to transmit data to Experian, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data. Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Experian meets any privacy or security obligations you may have. For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732). Your Dynamics 365 Customer Insights administrator can remove this enrichment at any time to discontinue use of this functionality.

## Configure the enrichment

1. Go to **Data** > **Enrichment** and select the **Discover** tab.

1. Select **Enrich my data** on the **Demographics** from Experian tile.

   :::image type="content" source="media/experian-tile.png" alt-text="Experian tile in the enrichment overview page. ":::

1. Review the overview and then select **Next**.

1. Select the connection. Contact an administrator if one is not available.

1. Select **Next**.

1. Select the **Customer data set** and choose the profile or segment you want to enrich with demographics data from Experian. The *Customer* entity enriches all your customer profiles whereas a segment enriches only customer profiles contained in that segment.

    :::image type="content" source="media/enrichment-Experian-configuration-customer-data-set.png" alt-text="Screenshot when choosing the customer data set.":::

1. Define which type of fields from your unified profiles to use for matching demographics data from Experian. At least one of the fields **Name and address**, **Phone**, or **Email** is required. For higher match accuracy, add other fields. Select **Next**.

1. Map your fields to the demographic data from Experian.

1. Select **Next** to complete the field mapping.

1. Provide a **Name** for the enrichment and the **Output entity name**.

1. Select **Save enrichment** after reviewing your choices.

1. Select **Run** to start the enrichment process or close to return to the **Enrichments** page.

## Enrichment results

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

The **Number of customers enriched by field** provides a drill-down into the coverage of each enriched field.

## Next steps

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
