# Create Ad Squads with Snapchat Ads

Creates new ad squads in Snapchat Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/adsquads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Ad Squads](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The Snapchat Campaign ID that will own the ad squads. |
| `adsquads` | body | `list<object>` | yes | An array of Snapchat ad squad objects to create. |
