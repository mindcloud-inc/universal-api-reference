# Search Templates By Text with Memix

Finds templates in Memix by text.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates/search`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Text to match against template text intent. |
| `limit` | query | `number` | no | Maximum number of templates to return. |
