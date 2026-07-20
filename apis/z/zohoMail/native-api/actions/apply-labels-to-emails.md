# Apply Labels To Emails with Zoho Mail

Applies labels to emails in Zoho Mail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/updatemessage`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Apply Labels To Emails](https://www.zoho.com/mail/help/api/add-tag-to-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `messageId[]` | body | `array<string>` | no | One or more message IDs to apply labels to. |
| `threadId[]` | body | `array<string>` | no | One or more thread IDs to apply labels to instead of specific message IDs. |
| `labelId[]` | body | `array<string>` | yes | One or more label IDs to apply to the selected emails. |
| `isFolderSpecific` | body | `boolean` | no | Whether this label update should be restricted to a specific folder. |
| `folderId` | body | `string` | no | Folder ID used when Folder Specific is true. |
| `isArchive` | body | `boolean` | no | Whether archived emails should also be included in this label action. |
