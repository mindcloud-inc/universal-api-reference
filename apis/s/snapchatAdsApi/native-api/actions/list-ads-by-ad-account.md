# List Ads by Ad Account with Snapchat Ads

Retrieves ads from Snapchat Ads by ad account.

## Endpoint

- **Method:** `GET`
- **Path:** `/adaccounts/:adAccountId/ads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Ads by Ad Account](https://developers.snap.com/api/marketing-api/Ads-API/ads)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the ads. |
