# Update workspace roles by role ID with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/workspace-role/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update workspace roles by role ID](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | — |
| `roleName` | body | `string` | yes | — |
