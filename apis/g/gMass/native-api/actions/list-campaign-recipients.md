# List Campaign Recipients with GMass

Retrieves recipients from a GMass campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:campaignId/recipients`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [List Campaign Recipients](https://api.gmass.co/docs#tag/Reports/operation/Reports_Recipients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `number` | yes |
| `stage` | query | `number` | no |
| `date` | query | `date` | no |
