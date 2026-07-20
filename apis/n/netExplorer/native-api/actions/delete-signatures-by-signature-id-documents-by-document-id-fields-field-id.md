# Delete Signature Field with NetExplorer

## Endpoint

- **Method:** `DELETE`
- **Path:** `/signatures/:signatureId/documents/:documentId/fields/:fieldId`
- **Base URL:** `{platformBaseUrl}/api`
- **Official documentation:** [Delete Signature Field](https://api.netexplorer.fr/v3/#signature.delete.delete field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `signatureId` | path | `string` | yes |
| `documentId` | path | `string` | yes |
| `fieldId` | path | `string` | yes |
