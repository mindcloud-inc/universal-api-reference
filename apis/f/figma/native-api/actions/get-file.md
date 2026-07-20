# Get File with Figma

Retrieves a Figma file by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:key`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get File](https://developers.figma.com/docs/rest-api/file-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Key of the file to retrieve. |
| `version` | query | `string` | no | Version ID to retrieve a specific historical file snapshot. |
| `ids` | query | `string` | no | Comma-separated node IDs to return only selected nodes. |
| `depth` | query | `number` | no | Maximum depth of node traversal to return. |
| `geometry` | query | `string` | no | Geometry payload mode to include in response. |
| `plugin_data` | query | `string` | no | Comma-separated plugin IDs to include plugin data for. |
| `branch_data` | query | `boolean` | no | Whether to include branch metadata in response. |
