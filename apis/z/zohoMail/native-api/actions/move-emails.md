# Move Emails with Zoho Mail

Moves emails to a folder in Zoho Mail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/updatemessage`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Move Emails](https://www.zoho.com/mail/help/api/move-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `messageId[]` | body | `array<string>` | no | One or more message IDs to move. |
| `threadId[]` | body | `array<string>` | no | One or more thread IDs to move instead of specific message IDs. |
| `destfolderId` | body | `string` | yes | Folder ID of the destination folder. |
| `isFolderSpecific` | body | `boolean` | no | Whether the move should be restricted to a specific source folder. |
| `folderId` | body | `string` | no | Source folder ID used when Folder Specific is true. |
| `isArchive` | body | `boolean` | no | Whether archived emails should also be included in the move action. |
