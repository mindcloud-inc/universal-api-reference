# Create Document with SignWell

Creates a new document in SignWell.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Create Document](https://developers.signwell.com/reference/post_api-v1-documents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `test_mode` | body | `boolean` | no |
| `draft` | body | `boolean` | no |
| `files[]` | body | `array<object>` | yes |
| `files[].name` | body | `string` | no |
| `files[].file_url` | body | `string` | yes |
| `recipients[]` | body | `array<object>` | yes |
| `recipients[].id` | body | `string` | yes |
| `recipients[].email` | body | `string` | yes |
| `recipients[].name` | body | `string` | no |
| `recipients[].placeholder_name` | body | `string` | no |
