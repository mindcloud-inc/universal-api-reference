# Create Topics with Zoho Campaigns

Creates marketing topics in Zoho Campaigns.

## Endpoint

- **Method:** `POST`
- **Path:** `/topics`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Create Topics](https://www.zoho.com/campaigns/help/developers/create-topics.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `details` | query | `string` | yes | Topic envelope in Zoho's documented `details` format. |
