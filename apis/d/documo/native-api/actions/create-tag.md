# Create Tag with Documo

Creates a new tag in Documo.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tag`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Create Tag](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tag name. |
| `color` | body | `string` | yes | Hex color with leading #. |
| `isPublic` | body | `boolean` | no | Whether the tag is visible to all account users. |
