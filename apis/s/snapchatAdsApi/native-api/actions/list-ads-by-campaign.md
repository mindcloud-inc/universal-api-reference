# List Ads by Campaign with Snapchat Ads

Retrieves ads from Snapchat Ads by campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/ads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Ads by Campaign](https://developers.snap.com/api/marketing-api/Ads-API/ads)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The Snapchat Campaign ID that owns the ads. |
