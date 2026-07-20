# Rename File with ImageKit.io

Renames an existing file in ImageKit.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/files/rename`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Rename File](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/rename-file)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filePath` | body | `string` | no |
| `newFileName` | body | `string` | no |
| `purgeCache` | body | `boolean` | no |
