# List Campaigns with Reddit Lead Ads

Retrieves campaigns for an ad account from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/ad_accounts/{ad_account_id}/campaigns`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Campaigns](https://ads-api.reddit.com/docs/v3/operations/list-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to list campaigns for. |
| `id` | query | `string` | no | Optional campaign ID filter. |
