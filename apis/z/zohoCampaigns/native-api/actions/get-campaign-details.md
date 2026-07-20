# Get Campaign Details with Zoho Campaigns

Retrieves campaign details from Zoho Campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/getcampaigndetails`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Get Campaign Details](https://www.zoho.com/campaigns/help/developers/campaign-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignkey` | query | `string` | yes | Campaign key from a recent-campaign response. |
| `campaigntype` | query | `string` | no | Campaign type for the selected campaign. Accepted values: `0`, `1`. |
