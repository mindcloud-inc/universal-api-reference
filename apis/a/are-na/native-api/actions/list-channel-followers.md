# List Channel Followers with Are.na

Retrieves followers for a channel in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `channels/:id/followers`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List Channel Followers](https://www.are.na/developers/explore/channel/followers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na channel ID or slug. |
