# Update Folder with Speak Ai

Updates an existing folder in Speak Ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/folder/:folderId`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Update Folder](https://docs.speakai.co/#c69a7f0e-1a72-4b5a-b56f-014a6b285113)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Speak Ai folder identifier. |
| `name` | body | `string` | yes | New folder name. |
