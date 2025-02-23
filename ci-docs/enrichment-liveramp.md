---
title: "LiveRamp identity data enrichment"
description: "Enrich customer profiles with LiveRamp data."
ms.date: 06/10/2022
ms.reviewer: mhart

ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
---

# Enrich customer profiles with identity data from LiveRamp (preview)

LiveRamp provides deterministic offline identity resolution and consolidation of customer data. You can map personal identifiers in your customer data to the AbiliTec identity graph and receive AbiliTec IDs. You can then use these IDs for better unification of your customer data.

## Supported countries/regions

We currently support enriching customer profiles with LiveRamp data in the United States only.

## Prerequisites

- An active LiveRamp subscription. To get a subscription, reach out to your LiveRamp account team or to [dynamics@liveramp.com](mailto:dynamics@liveramp.com) for more information.

- An active AbiliTec subscription with a client ID and secret to access the API. For more information, see [AbiliTec API Developer Hub](https://developers.liveramp.com/abilitec-api/).

- A LiveRamp [connection](connections.md) is [configured](#configure-the-connection-for-liveramp) by an administrator.

## Configure the connection for LiveRamp

You must be an [administrator](permissions.md#admin) in Customer Insights and have an active LiveRamp client ID and secret.

1. Select **Add connection** when configuring an enrichment, or go to **Admin** > **Connections** and select **Set up** on the LiveRamp tile.

   :::image type="content" source="media/liveramp-connection.png" alt-text="Configuration pane to set up the connection to the LiveRamp AbiliTec service. ":::

1. Enter a name for the connection and a valid LiveRamp client ID and a secret.

1. Review and provide your consent for [Data privacy and compliance](#data-privacy-and-compliance) by selecting **I agree**.

1. Select **Verify** to validate the configuration and then select **Save**.

### Data privacy and compliance

When you enable Dynamics 365 Customer Insights to transmit data to LiveRamp, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data. Microsoft will transfer such data at your instruction, but you're responsible for ensuring that LiveRamp meets any privacy or security obligations you may have. For more information, review the [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732). Your Dynamics 365 Customer Insights Administrator can remove this enrichment at any time to discontinue use of this functionality.

## Configure the enrichment

1. Go to **Data** > **Enrichment** and select the **Discover** tab.

1. Select **Enrich my data** on the **Identity** from LiveRamp tile.

   :::image type="content" source="media/liveramp-tile.png" alt-text="Identity tile in the enrichment overview page. ":::

1. Review the overview and then select **Next**.

1. Select the connection. Contact an administrator if one is not available.

1. Select **Next**.

1. Select the **Customer data set** and choose the profile or segment you want to enrich with identity data from LiveRamp. The *Customer* entity enriches all your customer profiles whereas a segment enriches only customer profiles contained in that segment.

1. Define which type of fields from your unified profiles to use for matching identity data from LiveRamp. At least one of the fields **Name and address**, **E-mail**, or **Phone** is required. For higher match accuracy, add other fields. Select **Next**.

1. Map your fields to the identification data from LiveRamp.

   :::image type="content" source="media/liveramp-data-mapping.png" alt-text="Data mapping options for the LiveRamp enrichment.":::

1. Select **Next** to complete the field mapping.

1. Provide a **Name** for the enrichment and the **Output entity name**.

1. Select **Save enrichment** after reviewing your choices.

1. Select **Run** to start the enrichment process or close to return to the **Enrichments** page.

## Enrichment results

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

The **Number of customers enriched by field** provides a drill-down into the coverage of each enriched field.

## Next steps

Build on top of your enriched customer data. Use the AbiliTec IDs to consolidate customer profiles into a person-based view.
[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
