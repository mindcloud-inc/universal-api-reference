# Download Attachment with Zoho Mail

Retrieves attachment content from Zoho Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId/messages/:messageId/attachments/:attachmentId`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Download Attachment](https://www.zoho.com/mail/help/api/get-attachment-content.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `folderId` | path | `string` | yes | Folder ID containing the email. |
| `messageId` | path | `string` | yes | Message ID of the email. |
| `attachmentId` | path | `string` | yes | Attachment ID to download. |
