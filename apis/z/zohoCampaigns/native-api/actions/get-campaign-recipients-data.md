# Get Campaign Recipients Data with Zoho Campaigns

Retrieves campaign recipient data from Zoho Campaigns.

## Endpoint

- **Method:** `POST`
- **Path:** `/getcampaignrecipientsdata`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Get Campaign Recipients Data](https://www.zoho.com/campaigns/help/developers/campaign-recipient-data.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignkey` | query | `string` | yes | Campaign key from a recent-campaign response. |
| `action` | query | `string` | yes | Recipient subset to fetch for the campaign. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
