# Delete Document with Google Docs

Permanently deletes a Google Docs document from Google Drive.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://www.googleapis.com/drive/v3/files/:fileId`
- **Base URL:** `https://docs.googleapis.com/v1/documents`
- **Official documentation:** [Delete Document](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `list<string>` | yes | ID of the document file to delete |
