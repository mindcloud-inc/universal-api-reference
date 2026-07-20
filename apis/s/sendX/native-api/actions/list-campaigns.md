# List Campaigns with SendX

## Endpoint

- **Method:** `GET`
- **Path:** `/campaign`
- **Base URL:** `https://api.sendx.io/api/v1/rest`
- **Official documentation:** [List Campaigns](https://docs.sendx.io/api-reference/campaign/get-all-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignType` | query | `string` | no | Filter campaigns by type: all, draft, scheduled, or sent. |
