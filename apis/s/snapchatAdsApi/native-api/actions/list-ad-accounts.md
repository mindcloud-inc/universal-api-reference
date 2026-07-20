# List Ad Accounts with Snapchat Ads

Retrieves ad accounts from Snapchat Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/adaccounts`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Ad Accounts](https://developers.snap.com/api/marketing-api/Ads-API/ad-accounts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | The Snapchat Organization ID that owns the ad accounts. |
