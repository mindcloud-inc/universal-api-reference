# Create Ads with Snapchat Ads

Creates new ads in Snapchat Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/adsquads/:adSquadId/ads`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Ads](https://developers.snap.com/api/marketing-api/Ads-API/ads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adSquadId` | path | `string` | yes | The Snapchat Ad Squad ID that will own the ads. |
| `ads` | body | `list<object>` | yes | An array of Snapchat ad objects to create. |
