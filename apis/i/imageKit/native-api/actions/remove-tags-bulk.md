# Remove Tags Bulk with ImageKit.io

Removes tags from multiple files in ImageKit.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/removeTags`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Remove Tags Bulk](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/remove-tags-bulk)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileIds` | body | `list<string>` | no |
| `tags` | body | `list<string>` | no |
