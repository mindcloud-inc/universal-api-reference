# List Documents with Google Docs

Finds Google Docs and Word documents in Google Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.googleapis.com/drive/v3/files`
- **Base URL:** `https://docs.googleapis.com/v1/documents`
- **Official documentation:** [List Documents](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | query | `list<string>` | no | Id of the folder |
