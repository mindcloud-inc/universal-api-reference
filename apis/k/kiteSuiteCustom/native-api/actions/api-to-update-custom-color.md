# Api to update custom color with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/custom-color/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Api to update custom color](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | custom color Id |
| `color` | body | `string` | yes | — |
