# List Child Mail Folders with Microsoft 365

Retrieves child mail folders from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/mailFolders/:mailFolderId/childFolders`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Child Mail Folders](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-childfolders?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailFolderId` | path | `list<string>` | yes | Choose the parent mail folder from the folder lookup. If you are not sure where to start, choose Inbox. |
| `$top` | query | `number` | no | Maximum number of child folders to return. |
| `includeHiddenFolders` | query | `boolean` | no | Whether to include hidden child folders in the results. |
