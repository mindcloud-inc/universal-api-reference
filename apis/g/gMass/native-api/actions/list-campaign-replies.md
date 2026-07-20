# List Campaign Replies with GMass

Retrieves recipients who replied to a GMass campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:campaignId/replies`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [List Campaign Replies](https://api.gmass.co/docs#tag/Reports/operation/Reports_Replies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `number` | yes |
