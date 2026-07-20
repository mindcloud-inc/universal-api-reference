# List Spreadsheets with Google Sheets

Retrieves accessible Google Sheets files from Google Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.googleapis.com/drive/v3/files`
- **Base URL:** `https://sheets.googleapis.com/v4`
- **Official documentation:** [List Spreadsheets](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | no |
| `supportsAllDrives` | query | `string` | no |
| `includeItemsFromAllDrives` | query | `string` | no |
