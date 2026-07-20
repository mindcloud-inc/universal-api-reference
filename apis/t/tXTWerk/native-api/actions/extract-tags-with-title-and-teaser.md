# Extract Tags With Title And Teaser with TXT Werk

Retrieves tags from text using title and teaser in TXT Werk.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/txt/analyzer`
- **Base URL:** `https://api.txtwerk.de`
- **Official documentation:** [Extract Tags With Title And Teaser](https://services.txtwerk.de/ws/documentation/showRequest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `language` | body | `string` | no |
| `title` | body | `string` | no |
| `teaser` | body | `string` | no |
| `ntags` | body | `number` | no |
