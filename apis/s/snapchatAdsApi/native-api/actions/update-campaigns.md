# Update Campaigns with Snapchat Ads

Updates existing campaigns in Snapchat Ads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/adaccounts/:adAccountId/campaigns`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Update Campaigns](https://developers.snap.com/api/marketing-api/Ads-API/campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the campaigns to update. |
| `campaigns` | body | `list<object>` | yes | An array of full Snapchat campaign objects to update. |
