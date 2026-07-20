# Delete Highlight with Glasp

Deletes a Glasp highlight or all highlights in a document.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/highlights/delete`
- **Base URL:** `https://api.glasp.co`
- **Official documentation:** [Delete Highlight](https://glasp.co/docs/apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Document URL that owns the highlight. |
| `highlight_id` | body | `string` | yes | Identifier of the Glasp highlight to delete. |
