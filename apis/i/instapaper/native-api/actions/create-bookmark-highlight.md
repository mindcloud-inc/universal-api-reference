# Create Bookmark Highlight with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.1/bookmarks/:bookmarkId/highlight`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [Create Bookmark Highlight](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmarkId` | path | `string` | yes | The bookmark where the highlight will be created. |
| `position` | body | `string` | no | Optional 0-indexed position of the text in the content. |
| `text` | body | `string` | yes | The highlight text. HTML tags should be unescaped. |
