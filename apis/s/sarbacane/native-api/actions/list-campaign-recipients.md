# List Campaign Recipients with Sarbacane

Retrieves recipients for a campaign in Sarbacane.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{campaignId}/recipients`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [List Campaign Recipients](https://developers.sarbacane.com/campaigns/#list-recipients-campaign)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | no | Sarbacane campaign ID. |
