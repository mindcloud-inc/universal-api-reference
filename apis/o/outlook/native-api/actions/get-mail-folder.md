# Get Mail Folder with Outlook

Retrieves an Outlook mail folder by folder ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/me/mailFolders/:folderId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Get Mail Folder](https://learn.microsoft.com/en-us/graph/api/mailfolder-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Microsoft Graph ID or well-known folder name, such as inbox, for the Outlook mail folder. |
