# List Attachments with SigningHub

Retrieves attachments from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/documents/:documentId/attachments`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [List Attachments](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_GetAttachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | Document ID of the document whose attachments are requested. |
| `packageId` | path | `number` | yes | Package ID of the package to which the document belongs. |
