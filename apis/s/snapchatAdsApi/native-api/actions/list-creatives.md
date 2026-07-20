# List Creatives with Snapchat Ads

Retrieves creatives from Snapchat Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/adaccounts/:adAccountId/creatives`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Creatives](https://developers.snap.com/api/marketing-api/Ads-API/creatives)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the creatives. |
