# Get Campaign with Campaign Cleaner

Retrieves a campaign from Campaign Cleaner.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get_campaign`
- **Base URL:** `https://api.campaigncleaner.com`
- **Official documentation:** [Get Campaign](https://docs.campaigncleaner.com/api-reference/endpoint/get-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign.id` | body | `string` | yes | The campaign ID to retrieve. |
| `campaign.minimize_html` | body | `boolean` | no | When enabled, removes extra whitespace from the returned campaign HTML to reduce payload size. |
