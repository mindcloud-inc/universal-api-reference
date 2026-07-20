# List Files with Trint

Retrieves files from your Trint account.

## Endpoint

- **Method:** `GET`
- **Path:** `/transcripts/`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [List Files](https://dev.trint.com/reference/page)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | query | `string` | no | When used with a shared drive, only list files inside the specified folder. |
| `sharedDriveId` | query | `string` | no | Only list files accessible via the specified shared drive. |
