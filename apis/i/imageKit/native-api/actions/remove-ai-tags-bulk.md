# Remove AI Tags Bulk with ImageKit.io

Removes AI tags from multiple files in ImageKit.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/removeAITags`
- **Base URL:** `https://api.imagekit.io/v1`
- **Official documentation:** [Remove AI Tags Bulk](https://imagekit.io/docs/api-reference/digital-asset-management-dam/managing-assets/remove-ai-tags-bulk)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AITags` | body | `list<string>` | no |
| `fileIds` | body | `list<string>` | no |
