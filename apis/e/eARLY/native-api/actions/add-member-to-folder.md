# Add Member to Folder with EARLY

Adds a member to an EARLY folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/folders/:folderId/members`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Add Member to Folder](https://developers.early.app/#379ec93f-802b-43f7-a12c-c7bbf7b51555)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID. |
| `email` | body | `string` | yes | Email address of the member to add. |
| `accessLevel` | body | `string` | yes | Folder access level. |
