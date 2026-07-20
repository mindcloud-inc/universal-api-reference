# List Campaigns with SuperSend

Retrieves campaigns from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Campaigns](https://docs.supersend.io/docs/campaign)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TeamId` | query | `string` | no | — |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
| `search` | query | `string` | no | — |
| `status` | query | `string` | no | Allowed values: active, inactive. |
