# Add Bookmark with Recombee

Creates a bookmark event in Recombee.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookmarks/`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Add Bookmark](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `itemId` | body | `string` | yes |
| `userId` | body | `string` | yes |
