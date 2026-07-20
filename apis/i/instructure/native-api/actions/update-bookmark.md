# Update Bookmark with Instructure

Updates an existing bookmark in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/bookmarks/:bookmark_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Bookmark](https://developerdocs.instructure.com/services/canvas/resources/bookmarks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmark_id` | path | `string` | yes | The Canvas bookmark ID. |
| `data` | body | `string` | no | Associated bookmark data. |
| `name` | body | `string` | no | The name of the bookmark. |
| `position` | body | `string` | no | The position of the bookmark. |
| `url` | body | `string` | no | The URL of the bookmark. |
