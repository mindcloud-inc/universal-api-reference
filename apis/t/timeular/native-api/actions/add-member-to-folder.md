# Add Member to Folder with Timeular

Adds a member to a folder in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/folders/:folderId/members`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Add Member to Folder](https://developers.early.app/#379ec93f-802b-43f7-a12c-c7bbf7b51555)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accessLevel` | body | `string` | no |
| `email` | body | `string` | yes |
| `folderId` | path | `string` | yes |
