# Update Pipe Node with Tinybird

## Endpoint

- **Method:** `PUT`
- **Path:** `v0/pipes/:name/nodes/:node`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Update Pipe Node](https://www.tinybird.co/docs/api-reference/pipe-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | Optional new node description |
| `name` | path | `string` | yes | The pipe name to target. |
| `name` | query | `string` | no | Optional new node name |
| `node` | path | `string` | yes | The pipe node name to target. |
| `sql` | body | `string` | yes | Replacement SQL for the transformation node |
