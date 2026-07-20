# Create Asset Folder with Shuffll

Creates a new asset folder in Shuffll.

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId/assets/folder`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Create Asset Folder](https://api-docs.shuffll.com/apis/assets/createassetfolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `newName` | body | `string` | yes | New folder name. |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |
