# Move Bookmark with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1/bookmarks/move`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [Move Bookmark](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmark_id` | body | `string` | yes | The bookmark to move. |
| `folder_id` | body | `string` | yes | The destination user-created folder. |
