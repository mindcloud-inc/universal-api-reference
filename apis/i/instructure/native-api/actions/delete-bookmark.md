# Delete Bookmark with Instructure

Deletes a bookmark from Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/self/bookmarks/:bookmark_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Delete Bookmark](https://developerdocs.instructure.com/services/canvas/resources/bookmarks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmark_id` | path | `string` | yes | The Canvas bookmark ID. |
