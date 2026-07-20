# Create Style Guide with Markup AI

Creates a new style guide in Markup AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/style-guides`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Create Style Guide](https://docs.markup.ai/api-reference/style-guides/create-style-guide)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_upload` | body | `file` | yes | Style guide file to upload. |
| `name` | body | `string` | yes | Name for the style guide. |
| `base_style_guide` | body | `string` | no | Optional base style guide identifier or preset. |
| `terminology_domain_ids[]` | body | `array<string>` | no | Optional terminology domain IDs to associate with the style guide. |
