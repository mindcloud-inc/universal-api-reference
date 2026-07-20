# Download Attachment with SigningHub

Downloads an attachment from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/documents/:documentId/attachments/:attachment_id`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Download Attachment](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Attachment_DownloadAttachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `number` | yes | ID of the attachment to download. |
| `documentId` | path | `number` | yes | Document ID of the document whose attachment is downloaded. |
| `packageId` | path | `number` | yes | Package ID of the package to which the document belongs. |
