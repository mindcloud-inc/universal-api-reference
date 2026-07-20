# List Ad Groups with Reddit Lead Ads

Retrieves ad groups for an ad account from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/ad_accounts/{ad_account_id}/ad_groups`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Ad Groups](https://ads-api.reddit.com/docs/v3/operations/list-ad-groups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to list ad groups for. |
| `campaign_id` | query | `string` | no | Optional campaign ID filter. |
| `id` | query | `string` | no | Optional ad group ID filter. |
