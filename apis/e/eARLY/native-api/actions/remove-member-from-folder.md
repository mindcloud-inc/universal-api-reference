# Remove Member from Folder with EARLY

Removes a member from an EARLY folder.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v4/folders/:folderId/members/:memberId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Remove Member from Folder](https://developers.early.app/#a1e03e9c-cf98-460c-ae95-e1b3626304b6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID. |
| `memberId` | path | `string` | yes | Folder member ID. |
