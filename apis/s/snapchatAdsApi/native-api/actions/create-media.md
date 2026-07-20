# Create Media with Snapchat Ads

Creates new media assets in Snapchat Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/media`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Media](https://developers.snap.com/api/marketing-api/Ads-API/media)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that will own the media. |
| `media` | body | `list<object>` | yes | An array of Snapchat media objects to create. |
