# Cancel Document with Eversign

Cancels an existing document in Eversign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Cancel Document](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cancel` | query | `string` | no |
| `document_hash` | query | `string` | yes |
