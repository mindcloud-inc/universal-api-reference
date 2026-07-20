# List Files with Minimax

Retrieves files from Minimax.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files/list`
- **Base URL:** `https://api.minimax.io`
- **Official documentation:** [List Files](https://platform.minimax.io/docs/api-reference/file-management-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purpose` | query | `list` | yes | The file purpose to list. Accepted values: `0`, `1`, `2`. |
