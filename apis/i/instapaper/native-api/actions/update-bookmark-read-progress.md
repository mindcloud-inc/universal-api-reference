# Update Bookmark Read Progress with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1/bookmarks/update_read_progress`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [Update Bookmark Read Progress](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmark_id` | body | `string` | yes | The bookmark whose reading progress you want to update. |
| `progress` | body | `string` | yes | Reading progress between 0.0 and 1.0. |
| `progress_timestamp` | body | `string` | yes | Unix timestamp when the progress was recorded. |
