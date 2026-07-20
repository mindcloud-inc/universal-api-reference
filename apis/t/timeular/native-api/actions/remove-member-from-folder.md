# Remove Member from Folder with Timeular

Removes a member from a folder in your Timeular workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v4/folders/:folderId/members/:memberId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Remove Member from Folder](https://developers.early.app/#a1e03e9c-cf98-460c-ae95-e1b3626304b6)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderId` | path | `string` | yes |
| `memberId` | path | `string` | yes |
