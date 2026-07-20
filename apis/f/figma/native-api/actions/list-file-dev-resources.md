# List File Dev Resources with Figma

Retrieves dev resources from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.figma.com/v1/files/:file_key/dev_resources`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [List File Dev Resources](https://developers.figma.com/docs/rest-api/dev-resources-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_key` | path | `string` | yes | Main Figma file key (not a branch key). |
| `node_ids` | query | `string` | no | Comma-separated node IDs to scope returned dev resources. |
