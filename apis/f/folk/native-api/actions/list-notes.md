# List Notes with folk

Retrieves a list of notes from folk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/notes`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [List Notes](https://developer.folk.app/api-reference/notes/list-notes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity.id` | query | `string` | no | Filter notes by entity. Only notes linked to the specified entity will be returned. |
