# Create Folder with LogMeIn

Creates a new knowledge base folder in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/resolve/knowledge-base/v2/folders`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Create Folder](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Required folder name. |
| `parentFolderId` | body | `string` | no | Optional parent folder ID. Omit for a root-level folder. |
