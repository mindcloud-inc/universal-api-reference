# List Folder Messages with Outlook

Retrieves emails from a specific Outlook mail folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/me/mailFolders/:folderId/messages`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List Folder Messages](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Microsoft Graph ID or well-known folder name, such as inbox, for the Outlook mail folder. |
