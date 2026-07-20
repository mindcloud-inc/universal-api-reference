# Create Saved Audience with Reddit Lead Ads

Creates a saved audience in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/saved_audiences`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Create Saved Audience](https://ads-api.reddit.com/docs/v3/operations/create-saved-audience)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to create the saved audience under. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
