# Update Folder with LogMeIn

Updates an existing knowledge base folder in LogMeIn.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/resolve/knowledge-base/v2/folders/:folderId`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Update Folder](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Required folder ID. |
| `name` | body | `string` | no | New folder name. |
| `parentFolderId` | body | `string` | no | New parent folder ID. |
