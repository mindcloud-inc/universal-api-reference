# List Files with Strategypoint

Retrieves files from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [List Files](https://developer.clearpointstrategy.com/reference/listfiles-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of files to return. |
| `search` | query | `string` | no | Search text to match files. |
| `start` | query | `number` | no | Offset into the file result set. |
| `userId` | query | `number` | no | Filter files by the uploading user. |
