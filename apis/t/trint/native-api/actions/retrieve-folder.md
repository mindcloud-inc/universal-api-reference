# Retrieve Folder with Trint

Retrieves a folder from your Trint account.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/folder`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Retrieve Folder](https://dev.trint.com/reference/retrieve-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | query | `string` | yes | The folder identifier to retrieve. |
| `workspaceId` | query | `string` | no | Shared drive identifier when the folder belongs to a shared drive. |
