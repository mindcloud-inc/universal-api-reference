# Query Pipe (POST) with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/pipes/:name.json`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Query Pipe (POST)](https://www.tinybird.co/docs/api-reference/pipe-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The published Pipe name. |
| `q` | body | `string` | no | Optional query parameters for the Pipe. |
