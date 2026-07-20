# Toggle Tool with OnceOnly

Updates a tool's enabled status in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tools/:name/toggle`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Toggle Tool](https://docs.onceonly.tech/reference/tools/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Tool name. |
| `enabled` | body | `boolean` | yes | Set to true to enable or false to disable. |
