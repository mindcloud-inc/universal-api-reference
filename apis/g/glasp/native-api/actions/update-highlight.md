# Update Highlight with Glasp

Updates an existing highlight in Glasp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/highlights/update`
- **Base URL:** `https://api.glasp.co`
- **Official documentation:** [Update Highlight](https://glasp.co/docs/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Document URL that owns the highlight. |
| `highlight_id` | body | `string` | yes | Identifier of the Glasp highlight to update. |
| `text` | body | `string` | no | Updated highlight text. |
| `note` | body | `string` | no | Updated note attached to the highlight. |
| `color` | body | `string` | no | Updated color for the highlight. |
| `location` | body | `number` | no | Updated highlight position within the document. |
| `highlight_url` | body | `string` | no | Updated canonical URL for the highlight. |
