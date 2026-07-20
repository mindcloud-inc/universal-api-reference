# Get Parent Folder with Google Drive

Returns a Parent Folder for a File or Folder in Google Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/files/:fileId`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Get Parent Folder](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Projection fields to return from files.get. Use this action to retrieve parent metadata via the parents field. |
| `fileId` | path | `string` | yes | The Id of a File to retrieve parent folders for. |
