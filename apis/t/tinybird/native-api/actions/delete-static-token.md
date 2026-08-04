# Delete Static Token with Tinybird

## Endpoint

- **Method:** `DELETE`
- **Path:** `v0/tokens/:token`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Delete Static Token](https://www.tinybird.co/docs/api-reference/token-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | path | `string` | yes | The required value is the static token itself, not its display name. |
