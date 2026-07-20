# Update Folder with Timeular

Updates an existing folder in your Timeular workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/folders/:folderId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Folder](https://developers.early.app/#40d2035a-6b0d-4b68-9259-6a4779a8928c)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderId` | path | `string` | yes |
| `name` | body | `string` | no |
