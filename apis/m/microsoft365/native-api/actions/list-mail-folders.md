# List Mail Folders with Microsoft 365

Retrieves mail folders from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/mailFolders`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Mail Folders](https://learn.microsoft.com/en-us/graph/api/user-list-mailfolders?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Upper bound on the number of top-level folders to return from the current page. If you set this low, folders like Inbox might not appear in the first page even though they exist. |
| `includeHiddenFolders` | query | `boolean` | no | Whether to include hidden mail folders in the results. |
