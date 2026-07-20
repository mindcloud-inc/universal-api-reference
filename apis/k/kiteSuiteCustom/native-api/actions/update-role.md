# Update Role with Kite Suite

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/project-role/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Role](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | — |
| `roleName` | body | `string` | yes | — |
