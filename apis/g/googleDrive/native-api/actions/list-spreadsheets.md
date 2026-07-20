# List Spreadsheets with Google Drive

Finds spreadsheets in Google Drive by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v3/files`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Spreadsheets](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderBy` | query | `string` | no | Optional Google Drive orderBy expression, such as modifiedTime desc or name. |
