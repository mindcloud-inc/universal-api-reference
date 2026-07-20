# Update Folder with EARLY

Updates a folder in EARLY.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/folders/:folderId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Folder](https://developers.early.app/#40d2035a-6b0d-4b68-9259-6a4779a8928c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID. |
| `name` | body | `string` | yes | Updated folder name. |
