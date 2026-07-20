# List Pixels By Ad Account with Reddit Lead Ads

Retrieves pixels for an ad account from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/ad_accounts/{ad_account_id}/pixels`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Pixels By Ad Account](https://ads-api.reddit.com/docs/v3/operations/list-pixels-by-ad-account)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to list pixels for. |
