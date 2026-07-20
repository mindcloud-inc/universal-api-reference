# Update Ads with Snapchat Ads

Updates existing ads in Snapchat Ads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/adsquads/:adSquadId/ads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Update Ads](https://developers.snap.com/api/marketing-api/Ads-API/ads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adSquadId` | path | `string` | yes | The Snapchat Ad Squad ID that owns the ads to update. |
| `ads` | body | `list<object>` | yes | An array of full Snapchat ad objects to update. |
