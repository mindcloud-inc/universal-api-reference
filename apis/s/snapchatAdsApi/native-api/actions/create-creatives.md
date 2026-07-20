# Create Creatives with Snapchat Ads

Creates new creatives in Snapchat Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/creatives`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Creatives](https://developers.snap.com/api/marketing-api/Ads-API/creatives)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that will own the creatives. |
| `creatives` | body | `list<object>` | yes | An array of Snapchat creative objects to create. |
