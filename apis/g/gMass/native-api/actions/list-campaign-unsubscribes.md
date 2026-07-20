# List Campaign Unsubscribes with GMass

Retrieves recipients who unsubscribed from a GMass campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:campaignId/unsubscribes`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [List Campaign Unsubscribes](https://api.gmass.co/docs#tag/Reports/operation/Reports_Unsubscribes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `number` | yes |
