# Create Folder with Zoho Mail

Creates a new folder in Zoho Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/folders`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Create Folder](https://www.zoho.com/mail/help/api/post-create-new-folder.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier returned by List Accounts. |
| `folderName` | body | `string` | yes | Unique folder name to create. Special characters are not allowed. |
| `parentFolderId` | body | `string` | no | Optional parent folder identifier. |
| `parentFolderPath` | body | `string` | no | Optional parent folder path. |
