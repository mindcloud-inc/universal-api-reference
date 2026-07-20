# Create Tag with Zaia

Creates a new tag in Zaia.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tags`
- **Base URL:** `https://api.endless.zaia.app`
- **Official documentation:** [Create Tag](https://docs.zaia.app/documentation/api-reference-alpha/reference/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `list` | yes | The color of the tag. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `description` | body | `string` | yes | The description of the tag. |
| `name` | body | `string` | yes | The display name of the tag. |
