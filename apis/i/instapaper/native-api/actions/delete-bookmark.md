# Delete Bookmark with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1/bookmarks/delete`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [Delete Bookmark](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmark_id` | body | `string` | yes | The bookmark to permanently delete. |
