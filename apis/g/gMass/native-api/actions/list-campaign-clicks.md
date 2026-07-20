# List Campaign Clicks with GMass

Retrieves recipients who clicked links in a GMass campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:campaignId/clicks`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [List Campaign Clicks](https://api.gmass.co/docs#tag/Reports/operation/Reports_Clicks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `number` | yes |
