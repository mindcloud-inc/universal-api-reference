# Search Files and Folders with Dropbox

Finds files and folders in Dropbox by search query.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/search_v2`
- **Base URL:** `https://api.dropboxapi.com/2`
- **Official documentation:** [Search Files and Folders](https://www.dropbox.com/developers/documentation/http/documentation#files-search_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The search string to look for across files and folders. |
| `options.path` | body | `string` | no | Optional folder path to scope the search. |
| `options.max_results` | body | `number` | no | Maximum number of matches to return, from 1 to 1000. |
| `options.filename_only` | body | `boolean` | no | When enabled, only file and folder names are searched. |
| `match_field_options.include_highlights` | body | `boolean` | no | When enabled, include title highlight spans in the match fields. |
