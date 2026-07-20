# Analyze Entity Candidates with TXT Werk

Retrieves entity candidates from text in TXT Werk.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/txt/analyzer`
- **Base URL:** `https://api.txtwerk.de`
- **Official documentation:** [Analyze Entity Candidates](https://services.txtwerk.de/ws/documentation/showRequest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `language` | body | `string` | no |
| `nentities` | body | `number` | no |
