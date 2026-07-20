# Get Attachment Info with Zoho Mail

Retrieves attachment info from Zoho Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId/messages/:messageId/attachmentinfo`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Get Attachment Info](https://www.zoho.com/mail/help/api/get-attach-info.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `folderId` | path | `string` | yes | Folder ID containing the email. |
| `messageId` | path | `string` | yes | Message ID of the email. |
| `includeInline` | query | `boolean` | no | Whether inline attachments should be included in the attachment info response. |
