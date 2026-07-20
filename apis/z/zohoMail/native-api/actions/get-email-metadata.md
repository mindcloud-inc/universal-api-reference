# Get Email Metadata with Zoho Mail

Retrieves email metadata from Zoho Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId/messages/:messageId/details`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Get Email Metadata](https://www.zoho.com/mail/help/api/get-email-meta-data.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `folderId` | path | `string` | yes | Folder ID containing the email. |
| `messageId` | path | `string` | yes | Message ID of the email. |
