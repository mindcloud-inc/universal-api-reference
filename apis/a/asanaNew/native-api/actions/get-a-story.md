# Get a story with Asana

Retrieves a story from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `stories/:story_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a story](https://developers.asana.com/reference/getstory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `offset` | query | `string` | no | — |
| `opt_fields[]` | query | `array<string>` | no | — |
| `story_gid` | path | `string` | yes | Path parameter: story_gid |
