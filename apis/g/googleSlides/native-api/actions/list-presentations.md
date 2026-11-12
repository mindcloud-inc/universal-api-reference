# List Presentations with Google Slides

Lists the Google Slides presentations the connection can access, excluding trashed files.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/files`
- **Base URL:** `https://www.googleapis.com`
- **API:** Google Drive API
- **Official documentation:** [List Presentations](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderBy` | query | `string` | no | Comma-separated sort keys: createdTime, folder, modifiedByMeTime, modifiedTime, name, name_natural, quotaBytesUsed, recency, sharedWithMeTime, starred, viewedByMeTime. Append desc to reverse a key. |
