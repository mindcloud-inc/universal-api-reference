# Update Pipe with Tinybird

## Endpoint

- **Method:** `PUT`
- **Path:** `v0/pipes/:name`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Update Pipe](https://www.tinybird.co/docs/api-reference/pipe-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | Optional new Pipe description |
| `name` | path | `string` | yes | The pipe name to target. |
| `name` | query | `string` | no | Optional new Pipe name |
