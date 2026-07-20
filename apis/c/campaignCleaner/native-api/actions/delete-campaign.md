# Delete Campaign with Campaign Cleaner

Deletes a campaign from Campaign Cleaner.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/delete_campaign`
- **Base URL:** `https://api.campaigncleaner.com`
- **Official documentation:** [Delete Campaign](https://docs.campaigncleaner.com/api-reference/endpoint/delete-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign.id` | body | `string` | yes | The campaign ID to delete. |
