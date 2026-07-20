# Delete Multiple Files with ImageKit.io

Deletes multiple files from the ImageKit.io media library.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/batch/deleteByFileIds`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Delete Multiple Files](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/delete-multiple-files)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileIds` | body | `list<string>` | no |
