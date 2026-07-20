# Trash Document with Eversign

Moves a document to trash in Eversign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Trash Document](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_hash` | query | `string` | yes |
| `trash` | query | `string` | no |
