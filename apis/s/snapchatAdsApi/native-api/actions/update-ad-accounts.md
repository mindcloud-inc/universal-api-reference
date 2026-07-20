# Update Ad Accounts with Snapchat Ads

Updates existing ad accounts in Snapchat Ads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:organizationId/adaccounts`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Update Ad Accounts](https://developers.snap.com/api/marketing-api/Ads-API/ad-accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | The Snapchat Organization ID that owns the ad accounts to update. |
| `adaccounts` | body | `list<object>` | yes | An array of Snapchat ad account objects to update. |
