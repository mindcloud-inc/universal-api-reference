# Get Ad Account History with Reddit Lead Ads

Retrieves the changelog for an ad account in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/history`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Get Ad Account History](https://ads-api.reddit.com/docs/v3/operations/get-ad-account-history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to get account history under. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
