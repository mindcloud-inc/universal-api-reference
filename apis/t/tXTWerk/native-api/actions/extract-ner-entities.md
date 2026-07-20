# Extract NER Entities with TXT Werk

Retrieves NER entities from text in TXT Werk.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/txt/analyzer`
- **Base URL:** `https://api.txtwerk.de`
- **Official documentation:** [Extract NER Entities](https://services.txtwerk.de/ws/documentation/showRequest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `language` | body | `string` | no |
