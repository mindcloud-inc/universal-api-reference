# Update Ad Squads with Snapchat Ads

Updates existing ad squads in Snapchat Ads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/:campaignId/adsquads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Update Ad Squads](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The Snapchat Campaign ID that owns the ad squads to update. |
| `adsquads` | body | `list<object>` | yes | An array of full Snapchat ad squad objects to update. |
