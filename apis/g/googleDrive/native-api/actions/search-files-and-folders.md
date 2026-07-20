# Search Files and Folders with Google Drive

Search Files & Folders in Google Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/files`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Search Files and Folders](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parents` | query | `list<string>` | no | Optionally, select a specific folder to search for files in. |
| `mimeType` | query | `list<string>` | no | Restrict the search to specific file types. If you want all file types, leave this field blank. |
| `searchType` | path | `list<string>` | no | Searching with 'Name' requires a Search Type. File Name Contains or File Name is Exactly. Use contains when looking for more than 1 file. Example, File Name Contains: 'PO# ' |
| `q` | query | `string` | no | Enter a File/Folder Name or type a phrase to search in file content. Example, "TEMPLATES". Then enter a "Search Type". |
| `fields` | query | `string` | no | — |
| `orderBy` | query | `string` | no | name,recency,etc. |
