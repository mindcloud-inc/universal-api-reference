# Create Ad with Reddit Lead Ads

Creates an ad in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/ads`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Create Ad](https://ads-api.reddit.com/docs/v3/operations/create-ad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to create the ad under. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
