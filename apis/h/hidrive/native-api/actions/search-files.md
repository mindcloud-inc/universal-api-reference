# Search Files with HiDrive

Finds files in HiDrive by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Search Files](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/search_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Filter by file category, such as directory. |
| `fields` | query | `string` | no | Comma-separated metadata fields to include. |
| `mime_type` | query | `string` | no | Filter by MIME type, such as image/*. |
| `path` | query | `string` | no | Search root path. |
| `pid` | query | `string` | no | HiDrive public ID for the search root. |
| `pattern` | query | `string<string>` | no | Filename pattern to search for. Repeat this parameter only if the API caller needs multiple patterns. |
| `limit` | query | `number` | no | Maximum number of search results. |
