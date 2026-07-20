# Rename Folder with ImageKit.io

Starts a folder rename job in ImageKit.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulkJobs/renameFolder`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Rename Folder](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/rename-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `folderPath` | body | `string` | no |
| `newFolderName` | body | `string` | no |
| `purgeCache` | body | `boolean` | no |
