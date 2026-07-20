# Update a Highlight with Histre

Updates a highlight in Histre.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/highlight/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Update a Highlight](https://histre.com/features/api/highlights/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `highlight_id` | body | `string` | yes | Identifier of the highlight to update. |
| `text` | body | `string` | yes | Updated highlighted text. |
| `color` | body | `string` | yes | Updated highlight color. |
| `extra` | body | `object` | no | Optional updated extra highlight details. |
| `note` | body | `string` | no | Optional updated note text. Pass null or empty string to remove it. |
