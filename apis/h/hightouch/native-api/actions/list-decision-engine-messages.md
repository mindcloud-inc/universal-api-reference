# List Decision Engine Messages with Hightouch

Retrieves decision engine messages from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/decision-engine/flow/{flowId}/messages`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [List Decision Engine Messages](https://api.hightouch.io/api/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `string` | yes | The Decision Engine flow ID. |
