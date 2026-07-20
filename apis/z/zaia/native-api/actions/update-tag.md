# Update Tag with Zaia

Updates an existing tag in Zaia.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/tags/:id`
- **Base URL:** `https://api.endless.zaia.app`
- **Official documentation:** [Update Tag](https://docs.zaia.app/documentation/api-reference-alpha/reference/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The UUID of the tag to update. |
| `color` | body | `list` | no | The color of the tag. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `description` | body | `string` | no | The description of the tag. |
| `name` | body | `string` | no | The display name of the tag. |
