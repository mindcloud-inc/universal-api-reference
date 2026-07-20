# Get Campaign Status with Campaign Cleaner

Retrieves a campaign's status from Campaign Cleaner.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get_campaign_status`
- **Base URL:** `https://api.campaigncleaner.com`
- **Official documentation:** [Get Campaign Status](https://docs.campaigncleaner.com/api-reference/endpoint/get-campaign-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign.id` | body | `string` | yes | The campaign ID to check. |
