# Get Document Verification with SigningHub

Retrieves document verification details from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/documents/:documentId/verification`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Get Document Verification](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Documents_GetVerification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | The document ID to verify. |
| `packageId` | path | `number` | yes | Package ID of the package to which the document belongs. |
