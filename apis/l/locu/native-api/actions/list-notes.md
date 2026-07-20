# List Notes with Locu

Retrieves a paginated list of notes from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Notes](https://locu.app/api/docs#tag/notes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | query | `string` | no | Filter notes by folder ID |
