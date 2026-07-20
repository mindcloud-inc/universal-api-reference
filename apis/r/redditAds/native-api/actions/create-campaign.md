# Create Campaign with Reddit Lead Ads

Creates a campaign in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/campaigns`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Create Campaign](https://ads-api.reddit.com/docs/v3/operations/create-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to create the campaign under. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
