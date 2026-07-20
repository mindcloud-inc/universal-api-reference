# List Group Contents with Are.na

Retrieves contents created by a group in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `groups/:id/contents`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List Group Contents](https://www.are.na/developers/explore/group/contents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na group ID. |
| `type` | query | `string` | no | Optional group content type filter. |
