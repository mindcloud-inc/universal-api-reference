# Fetch Media by IDs with Snapchat Ads

Retrieves media assets from Snapchat Ads by media IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/get_media_by_ids`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Fetch Media by IDs](https://developers.snap.com/api/marketing-api/Ads-API/media)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the media. |
| `media_ids` | body | `list<string>` | yes | An array of Snapchat Media IDs to fetch. |
