# Add Tags Bulk with ImageKit.io

Adds tags to multiple files in ImageKit.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/addTags`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Add Tags Bulk](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/add-tags-bulk)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileIds` | body | `list<string>` | no |
| `tags` | body | `list<string>` | no |
