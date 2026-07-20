# Delete Tag with Inoreader

Deletes an existing tag from Inoreader.

## Endpoint

- **Method:** `POST`
- **Path:** `/disable-tag`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [Delete Tag](https://www.inoreader.com/developers/delete-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | body | `string` | yes | Tag stream ID to delete or disable. |
