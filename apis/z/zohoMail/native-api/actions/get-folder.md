# Get Folder with Zoho Mail

Retrieves a folder from Zoho Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Get Folder](https://www.zoho.com/mail/help/api/get-single-folder-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier returned by List Accounts. |
| `folderId` | path | `string` | yes | Folder identifier returned by List Folders. |
