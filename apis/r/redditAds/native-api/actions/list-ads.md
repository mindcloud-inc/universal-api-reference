# List Ads with Reddit Lead Ads

Retrieves ads for an ad account from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/ad_accounts/{ad_account_id}/ads`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Ads](https://ads-api.reddit.com/docs/v3/operations/list-ads)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to list ads for. |
| `id` | query | `string` | no | Optional ad ID filter. |
