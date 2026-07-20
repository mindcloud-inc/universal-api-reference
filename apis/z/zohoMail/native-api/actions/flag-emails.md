# Flag Emails with Zoho Mail

Flags email messages in Zoho Mail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/updatemessage`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Flag Emails](https://www.zoho.com/mail/help/api/set-flag-for-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `messageId[]` | body | `array<string>` | no | One or more message IDs to flag. |
| `threadId[]` | body | `array<string>` | no | One or more thread IDs to flag instead of specific message IDs. |
| `flagid` | body | `list<string>` | yes | Flag to apply to the selected emails. Accepted values: `flag_not_set`, `followup`, `important`, `info`. |
| `isFolderSpecific` | body | `boolean` | no | Whether the flag update should be restricted to a specific folder. |
| `folderId` | body | `string` | no | Folder ID used when Folder Specific is true. |
| `isArchive` | body | `boolean` | no | Whether archived emails should also be included in the flag action. |
