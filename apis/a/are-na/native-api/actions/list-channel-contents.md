# List Channel Contents with Are.na

Retrieves contents from a channel in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `channels/:id/contents`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List Channel Contents](https://www.are.na/developers/explore/channel/contents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na channel ID or slug. |
