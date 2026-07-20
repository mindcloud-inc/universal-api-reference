# List Ads by Ad Squad with Snapchat Ads

Retrieves ads from Snapchat Ads by ad squad.

## Endpoint

- **Method:** `GET`
- **Path:** `/adsquads/:adSquadId/ads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Ads by Ad Squad](https://developers.snap.com/api/marketing-api/Ads-API/ads)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adSquadId` | path | `string` | yes | The Snapchat Ad Squad ID that owns the ads. |
