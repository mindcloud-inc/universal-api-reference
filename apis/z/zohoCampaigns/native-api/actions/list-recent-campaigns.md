# List Recent Campaigns with Zoho Campaigns

Retrieves recent campaigns from Zoho Campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/recentcampaigns`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [List Recent Campaigns](https://www.zoho.com/campaigns/help/developers/recent-campaign.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort order for the recent campaigns list. Accepted values: `0`, `1`. |
| `fromindex` | query | `number` | no | Starting index for the campaign list. |
| `range` | query | `number` | no | Maximum number of campaigns to return. |
| `status` | query | `string` | no | Campaign status filter. Accepted values: `0`, `1`, `10`, `11`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
