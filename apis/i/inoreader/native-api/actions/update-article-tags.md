# Update Article Tags with Inoreader

Updates article tags in Inoreader.

## Endpoint

- **Method:** `POST`
- **Path:** `/edit-tag`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [Update Article Tags](https://www.inoreader.com/developers/edit-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | body | `string` | yes | One or more article IDs to update. Send multiple values as a array. |
| `a` | body | `string` | no | System or custom tag to add to the item. |
| `r` | body | `string` | no | System or custom tag to remove from the item. |
