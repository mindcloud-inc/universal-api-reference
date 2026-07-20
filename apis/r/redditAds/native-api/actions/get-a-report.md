# Get A Report with Reddit Lead Ads

Generates a metrics report in Reddit Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/ad_accounts/{ad_account_id}/reports`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [Get A Report](https://ads-api.reddit.com/docs/v3/operations/get-a-report)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_account_id` | path | `string` | yes | The ID of the ad account to get the ads report under. |
| `data` | body | `object` | yes | JSON request body from the Reddit Ads API spec. |
