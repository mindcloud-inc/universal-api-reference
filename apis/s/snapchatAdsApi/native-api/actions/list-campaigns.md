# List Campaigns with Snapchat Ads

Retrieves campaigns from Snapchat Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/adaccounts/:adAccountId/campaigns`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Campaigns](https://developers.snap.com/api/marketing-api/Ads-API/campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | The Snapchat Ad Account ID that owns the campaigns. |
