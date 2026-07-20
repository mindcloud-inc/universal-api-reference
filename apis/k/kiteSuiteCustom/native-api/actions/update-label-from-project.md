# Update label from project. with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/label/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update label from project.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Project ID |
| `label` | body | `string` | yes | — |
