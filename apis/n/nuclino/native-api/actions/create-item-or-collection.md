# Create item or collection with Nuclino

Creates a new item or collection in Nuclino.

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://api.nuclino.com/v0`
- **Official documentation:** [Create item or collection](https://help.nuclino.com/fa38d15f-items-and-collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | — |
| `index` | body | `string` | no | Zero-based position within the parent. |
| `object` | body | `string` | no | Set to "collection" to create a collection instead of an item. |
| `parentId` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `workspaceId` | body | `string` | no | — |
