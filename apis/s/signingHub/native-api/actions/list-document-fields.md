# List Document Fields with SigningHub

Retrieves document fields from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/documents/:documentId/fields/:pageNo`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [List Document Fields](https://manuals.nsignhub.com/latest/Api/#tag/Document-Preparation/operation/V4_Fields_GetAllDocumentFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | The ID of the document whose fields are requested. |
| `packageId` | path | `number` | yes | The ID of the package to which the document belongs. |
| `pageNo` | path | `number` | yes | Page number of the document whose fields are requested. |
