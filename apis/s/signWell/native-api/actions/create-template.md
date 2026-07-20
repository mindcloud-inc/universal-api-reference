# Create Template with SignWell

Creates a new template in SignWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/document_templates`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Create Template](https://developers.signwell.com/reference/post_api-v1-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `test_mode` | body | `boolean` | no | — |
| `files[]` | body | `array<object>` | yes | — |
| `files[].name` | body | `string` | yes | — |
| `files[].file_url` | body | `string` | no | Public URL for the template file. Provide either File URL or File Base64, not both. |
| `files[].file_base64` | body | `string` | no | Base64-encoded file content for the template file. Provide either File URL or File Base64, not both. |
| `placeholders[]` | body | `array<object>` | yes | — |
| `placeholders[].id` | body | `string` | yes | — |
| `placeholders[].name` | body | `string` | yes | — |
