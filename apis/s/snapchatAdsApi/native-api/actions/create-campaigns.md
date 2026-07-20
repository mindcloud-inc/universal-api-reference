# Create Campaigns with Snapchat Ads

Creates new campaigns in Snapchat Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `/adaccounts/:adAccountId/campaigns`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Create Campaigns](https://developers.snap.com/api/marketing-api/Ads-API/campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that will own the campaigns. |
| `campaigns` | body | `list<object>` | yes | An array of Snapchat campaign objects to create. |
