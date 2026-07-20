# Create File with Google Drive

Creates a new file in Google Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v3/files`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Create File](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Give your new File a new Name. |
| `useContentAsIndexableText` | query | `boolean` | no | Whether to use the uploaded content as indexable text. Format: `toggle`. |
| `fileType` | body | `list<string>` | yes | Choose which Google Workspace file type to create. Accepted values: `document`, `form`, `fusiontable`, `presentation`, `spreadsheet`. |
| `ignoreDefaultVisibility` | query | `boolean` | no | Whether to ignore the domain's default visibility settings for the created file. Domain administrators can choose to make all uploaded files visible to the domain by default; this parameter bypasses that behavior for the request. Permissions are still inherited from parent folders. |
| `parents` | body | `list<string>` | no | The ID of a Google Drive Folder to place your file. When not specified files are added to your My Drive. Send multiple values as a array. |
