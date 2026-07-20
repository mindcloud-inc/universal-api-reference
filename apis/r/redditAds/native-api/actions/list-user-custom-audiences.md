# List User Custom Audiences with Reddit Lead Ads

Retrieves custom audiences for an ad account from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/ad_accounts/{ad_account_id}/custom_audiences`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List User Custom Audiences](https://ads-api.reddit.com/docs/v3/operations/list-user-custom-audiences)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the parent ad account. |
| `name` | query | `string` | no | Optional custom audience name filter. |
