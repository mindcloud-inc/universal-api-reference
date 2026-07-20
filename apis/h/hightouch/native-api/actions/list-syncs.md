# List Syncs with Hightouch

Retrieves syncs from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/syncs`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [List Syncs](https://api.hightouch.io/api/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | no | Filter syncs by slug. |
| `modelId` | query | `number` | no | Filter syncs by model ID. |
| `after` | query | `date` | no | Select syncs that were run after this ISO timestamp. |
| `before` | query | `date` | no | Select syncs that were run before this ISO timestamp. |
