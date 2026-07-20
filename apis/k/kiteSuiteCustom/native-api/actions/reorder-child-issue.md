# Reorder child issue with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/epic/task/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Reorder child issue](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | issue ID |
| `position` | body | `string` | yes | — |
