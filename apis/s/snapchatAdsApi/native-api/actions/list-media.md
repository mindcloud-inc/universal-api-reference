# List Media with Snapchat Ads

Retrieves media assets from Snapchat Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/adaccounts/:adAccountId/media`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Media](https://developers.snap.com/api/marketing-api/Ads-API/media)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the media. |
