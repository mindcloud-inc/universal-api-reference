# File Search And Replace Text with Encodian - General

Searches and replaces text in a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/SearchAndReplaceText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [File Search And Replace Text](https://support.encodian.com/hc/en-gb/articles/360020937853-Search-and-Replace-Text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileName` | body | `string` | no | Source filename including extension. |
| `FileContent` | body | `string` | no | Base64-encoded source file content. |
| `Phrases` | body | `list<object>` | yes | Array of search and replacement phrase objects. |
