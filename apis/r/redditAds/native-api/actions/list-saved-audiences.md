# List Saved Audiences with Reddit Lead Ads

Retrieves saved audiences from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/ad_accounts/{ad_account_id}/saved_audiences`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Saved Audiences](https://ads-api.reddit.com/docs/v3/operations/list-saved-audiences)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to list saved audiences for. |
