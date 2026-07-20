# Create Bookmark with Instructure

Creates a new bookmark in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/self/bookmarks`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Bookmark](https://developerdocs.instructure.com/services/canvas/resources/bookmarks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | no | Associated bookmark data. |
| `name` | body | `string` | no | The name of the bookmark. |
| `position` | body | `string` | no | The position of the bookmark. |
| `url` | body | `string` | no | The URL of the bookmark. |
