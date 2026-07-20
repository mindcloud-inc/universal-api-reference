# Move Folder with ImageKit.io

Starts a folder move job in ImageKit.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulkJobs/moveFolder`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Move Folder](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/move-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `destinationPath` | body | `string` | no |
| `sourceFolderPath` | body | `string` | no |
