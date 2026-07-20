# Delete Attachment with SigningHub

Deletes an attachment from SigningHub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v4/packages/:packageId/documents/:documentId/attachments/:attachmentId`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Delete Attachment](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_DeleteAttachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package containing the attachment to delete. |
| `documentId` | path | `number` | yes | The document containing the attachment to delete. |
| `attachmentId` | path | `number` | yes | The attachment to delete. |
