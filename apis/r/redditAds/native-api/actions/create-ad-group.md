# Create Ad Group with Reddit Lead Ads

Creates an ad group in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/ad_groups`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Create Ad Group](https://ads-api.reddit.com/docs/v3/operations/create-ad-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to create the ad group under. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
