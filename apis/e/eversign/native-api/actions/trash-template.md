# Trash Template with Eversign

Moves a template to trash in Eversign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Trash Template](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_hash` | query | `string` | yes |
| `trash` | query | `string` | no |
