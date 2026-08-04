# Add Pipe Node with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/pipes/:name/nodes`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Add Pipe Node](https://www.tinybird.co/docs/api-reference/pipe-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | Optional node description |
| `name` | path | `string` | yes | The pipe name to target. |
| `name` | query | `string` | no | New node name |
| `sql` | body | `string` | yes | SQL for the new transformation node |
