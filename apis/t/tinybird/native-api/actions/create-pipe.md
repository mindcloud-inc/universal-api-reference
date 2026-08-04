# Create Pipe with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/pipes`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Create Pipe](https://www.tinybird.co/docs/api-reference/pipe-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | Optional Pipe description |
| `name` | query | `string` | yes | New Pipe name |
| `sql` | query | `string` | yes | SQL for the Pipe's first transformation node |
