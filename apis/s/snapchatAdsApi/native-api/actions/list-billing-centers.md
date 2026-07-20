# List Billing Centers with Snapchat Ads

Retrieves billing centers from Snapchat Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/billingcenters`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [List Billing Centers](https://developers.snap.com/api/marketing-api/Ads-API/billing-centers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | The Snapchat Organization ID that owns the billing centers. |
