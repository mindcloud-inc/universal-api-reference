# Get Email Content with Zoho Mail

Retrieves email content from Zoho Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId/messages/:messageId/content`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Get Email Content](https://www.zoho.com/mail/help/api/get-email-content.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `folderId` | path | `string` | yes | Folder ID containing the email. |
| `messageId` | path | `string` | yes | Message ID of the email. |
| `includeBlockContent` | query | `boolean` | no | Whether blocked content should be included in the email body response. |
