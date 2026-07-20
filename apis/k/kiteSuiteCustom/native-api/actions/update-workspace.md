# Update workspace with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/workspace/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update workspace](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | workspace ID |
| `name` | body | `string` | no | — |
| `key` | body | `string` | no | — |
