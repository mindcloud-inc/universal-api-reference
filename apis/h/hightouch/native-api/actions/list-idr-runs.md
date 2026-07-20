# List IDR Runs with Hightouch

Retrieves IDR runs from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/idr/{graphId}/runs`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [List IDR Runs](https://api.hightouch.io/api/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `graphId` | path | `string` | yes | The IDR graph ID. |
| `runId` | query | `string` | no | Filter IDR runs by run ID. |
| `after` | query | `date` | no | Select IDR runs after this ISO timestamp. |
| `before` | query | `date` | no | Select IDR runs before this ISO timestamp. |
