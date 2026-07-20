# List Note Templates with LunaNotes

Retrieves note templates from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/note-templates`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Note Templates](https://lunanotes.io/docs/note-templates/get-v1-note-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `systemTemplateId` | query | `string` | no | Filter by source system template ID. |
| `title` | query | `string` | no | Search templates by title using a partial match. |
