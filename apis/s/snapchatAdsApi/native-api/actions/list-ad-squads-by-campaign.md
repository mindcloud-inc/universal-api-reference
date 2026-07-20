# List Ad Squads by Campaign with Snapchat Ads

Retrieves ad squads from Snapchat Ads by campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/adsquads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Ad Squads by Campaign](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The Snapchat Campaign ID that owns the ad squads. |
