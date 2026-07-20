# Copy Folder with ImageKit.io

Starts a folder copy job in ImageKit.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulkJobs/copyFolder`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Copy Folder](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-folders/copy-folder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `destinationPath` | body | `string` | no |
| `includeVersions` | body | `boolean` | no |
| `sourceFolderPath` | body | `string` | no |
