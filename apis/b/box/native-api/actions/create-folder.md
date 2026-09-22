# Create Folder with Box

## Endpoint

- **Method:** `POST`
- **Path:** `/folders`
- **Base URL:** `https://api.box.com/2.0`
- **Official documentation:** [Create Folder](https://developer.box.com/reference/post-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the new folder. |
| `parentFolderId` | body | `string` | yes | Parent Box folder ID. Use `0` to create the folder in the root folder. |
| `fields` | query | `string` | no | Optional comma-separated list of folder fields to include in the response. |
