# List Files with Google Drive

List all Files in your Google Drive. Does not return Folders. Optionally filter for a specific file.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/files`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Files](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Drive response field mask. The default includes file links and card metadata. Preserve nextPageToken when overriding to keep pagination available. |
| `q` | query | `string` | no | — |
| `parentId` | query | `list<string>` | no | Optionally, return only the folders inside a specified folder. Choose an option from the list or map a 'folderId' here. |
| `orderBy` | query | `string` | no | — |
