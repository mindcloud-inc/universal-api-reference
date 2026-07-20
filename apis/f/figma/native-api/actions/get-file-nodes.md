# Get File Nodes with Figma

Retrieves nodes from a Figma file by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:key/nodes`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get File Nodes](https://developers.figma.com/docs/rest-api/file-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Key of the file to read nodes from. |
| `ids` | query | `string` | yes | Comma-separated node IDs to fetch. |
| `version` | query | `string` | no | Version ID to fetch nodes from. |
| `depth` | query | `number` | no | Maximum depth of node traversal. |
| `geometry` | query | `string` | no | Geometry payload mode to include in response. |
| `plugin_data` | query | `string` | no | Comma-separated plugin IDs to include plugin data for. |
