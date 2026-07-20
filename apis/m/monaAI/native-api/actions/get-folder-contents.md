# Get Folder Contents with Mona AI

Retrieves folder contents from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/companyKnowledge/getFolderContents`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Folder Contents](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | body | `string` | yes | Knowledge folder identifier to inspect. |
| `includeFiles` | body | `boolean` | no | Whether to include files in folder contents. |
| `includeSubfolders` | body | `boolean` | no | Whether to include nested folders. |
| `permission` | body | `string` | yes | Mona permission string required by the folder contents endpoint. |
