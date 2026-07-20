# Get Bookmark with Instructure

Retrieves a bookmark from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/self/bookmarks/:bookmark_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Bookmark](https://developerdocs.instructure.com/services/canvas/file.all_resources/bookmarks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmark_id` | path | `string` | yes | The Canvas bookmark ID. |
