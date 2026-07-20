# Get General Document with MoneyBird

Retrieves a general document from MoneyBird.

## Endpoint

- **Method:** `GET`
- **Path:** `/:administrationId/documents/general_documents/:generalDocumentId.json`
- **Base URL:** `https://moneybird.com/api/v2`
- **Official documentation:** [Get General Document](https://developer.moneybird.com/api/documents-general-documents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `administrationId` | path | `string` | yes | Moneybird administration ID. |
| `generalDocumentId` | path | `string` | yes | Moneybird general document ID. |
