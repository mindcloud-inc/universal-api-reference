# Create Custom Audience with Reddit Lead Ads

Creates a custom audience in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/custom_audiences`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Create Custom Audience](https://ads-api.reddit.com/docs/v3/operations/create-custom-audience)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the parent ad account. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
