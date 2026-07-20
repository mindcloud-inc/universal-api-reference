# List Notes with LunaNotes

Retrieves notes from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/notes`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Notes](https://lunanotes.io/docs/notes/get-v1-notes)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft` | query | `boolean` | no | Filter by draft status. |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `isPublic` | query | `boolean` | no | Filter by public visibility status. |
| `status` | query | `string` | no | Filter by note lifecycle status. |
