# Delete Email with Zoho Mail

Deletes an email from Zoho Mail.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts/:accountId/folders/:folderId/messages/:messageId`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Delete Email](https://www.zoho.com/mail/help/api/delete-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID containing the email to delete. |
| `folderId` | path | `string` | yes | Folder ID containing the email to delete. |
| `messageId` | path | `string` | yes | Message ID of the email to delete. |
| `expunge` | query | `boolean` | no | Whether to permanently delete the email instead of moving it to Trash. |
