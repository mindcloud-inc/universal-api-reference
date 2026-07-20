# Create Tag with Dub

Creates a tag in Dub.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Create Tag](https://dub.co/docs/api-reference/tags/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tag display name. |
| `color` | body | `string` | no | Optional tag color. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
