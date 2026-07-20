# Move Template to Folder with Templated

Moves a template to a folder in Templated.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/folder/:folderId/template/:templateId`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [Move Template to Folder](https://templated.io/docs/folders/template/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | The folder where you want to move the template. |
| `templateId` | path | `string` | yes | The template you want to move into the folder. |
