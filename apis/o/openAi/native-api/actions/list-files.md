# List Files with Open AI

Retrieves files from Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/files`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [List Files](https://developers.openai.com/api/reference/files/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of files to return. |
| `order` | query | `string` | no | Sort order by created time. |
| `purpose` | query | `string` | no | Only return files with the given purpose. |
