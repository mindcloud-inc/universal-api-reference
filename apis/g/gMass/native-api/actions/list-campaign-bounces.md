# List Campaign Bounces with GMass

Retrieves recipients whose emails bounced in a GMass campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:campaignId/bounces`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [List Campaign Bounces](https://api.gmass.co/docs#tag/Reports/operation/Reports_Bounces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `number` | yes |
