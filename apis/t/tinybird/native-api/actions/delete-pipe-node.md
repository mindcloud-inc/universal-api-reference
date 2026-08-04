# Delete Pipe Node with Tinybird

## Endpoint

- **Method:** `DELETE`
- **Path:** `v0/pipes/:name/nodes/:node`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Delete Pipe Node](https://www.tinybird.co/docs/api-reference/pipe-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The pipe name to target. |
| `node` | path | `string` | yes | The pipe node name to target. |
