# Move Project to a Folder with Filestage

Moves a Filestage project to a folder.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{projectId}/folder`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Move Project to a Folder](https://developers.filestage.io/docs/api/yc164fkzqem9p-move-project-to-a-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | — |
| `folderId` | body | `string` | yes | The ID of the folder to move the project into. |
