# Update Tag with lc.cx

Updates an existing tag in lc.cx.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tags/update/:id`
- **Base URL:** `https://api.lc.cx/v1`
- **Official documentation:** [Update Tag](https://dev.lc.cx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the tag to update. |
| `name` | body | `string` | yes | The new name for the tag. |
| `color` | body | `string` | no | An optional hexadecimal color for the tag. |
