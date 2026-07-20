# List Campaign Blocks with GMass

Retrieves blocked recipients from a GMass campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:campaignId/blocks`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [List Campaign Blocks](https://api.gmass.co/docs#tag/Reports/operation/Reports_Blocks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `number` | yes |
