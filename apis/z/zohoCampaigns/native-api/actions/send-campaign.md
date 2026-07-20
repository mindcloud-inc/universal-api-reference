# Send Campaign with Zoho Campaigns

Sends a campaign in Zoho Campaigns.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendcampaign`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Send Campaign](https://www.zoho.com/campaigns/help/developers/send-campaign.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignkey` | query | `string` | yes | Campaign key from a recent-campaign response. |
