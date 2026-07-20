# Get Files with zipBoard

Retrieves files from zipBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Get Files](https://help.zipboard.co/article/179-api-for-files-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Owner` | body | `boolean` | no | Return files created by the authenticated user. |
| `projectid` | body | `string` | no | Optional project ID to return files for. |
| `projectid` | query | `string` | yes | — |
