# Upload Attachment with SigningHub

Uploads an attachment to SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/documents/:documentId/attachments`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Upload Attachment](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_UploadAttachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID of the package to which the document is added. |
| `documentId` | path | `number` | yes | ID of the document to which the attachment needs to be added. |
| `file (binary Stream)` | body | `string` | yes | Raw binary attachment content to upload. |
