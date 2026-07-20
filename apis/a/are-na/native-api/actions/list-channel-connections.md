# List Channel Connections with Are.na

Retrieves connections for a channel in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `channels/:id/connections`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List Channel Connections](https://www.are.na/developers/explore/channel/connections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na channel ID or slug. |
