# Update Tag with Dub

Updates a tag in Dub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tags/:id`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Update Tag](https://dub.co/docs/api-reference/tags/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Dub tag ID to update. |
| `name` | body | `string` | no | Updated tag name. |
| `color` | body | `string` | no | Updated tag color. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
