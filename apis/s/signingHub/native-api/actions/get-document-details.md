# Get Document Details with SigningHub

Retrieves document details from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/documents/:documentId/details`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Get Document Details](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_GetDocumentDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | The document ID for which the details are requested. |
| `packageId` | path | `number` | yes | The package ID of the package to which the document belongs. |
