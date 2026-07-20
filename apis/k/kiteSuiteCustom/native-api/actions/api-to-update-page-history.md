# Api to update page history with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/history/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Api to update page history](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | page Id |
| `name` | body | `string` | yes | — |
