# Export File with Google Drive

Exports a Google Workspace document from Google Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/files/:fileId/export`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Export File](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `list` | yes | Select a Google Workspace file to export. With drive.file access, Google only allows files created by or explicitly authorized to the app. |
| `mimeType` | query | `list` | yes | The export format to request from Google Drive files.export. Accepted values: `application/pdf`, `application/rtf`, `application/vnd.oasis.opendocument.text`, `application/vnd.openxmlformats-officedocument.presentationml.presentation`, `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`, `application/vnd.openxmlformats-officedocument.wordprocessingml.document`, `text/plain`. |
