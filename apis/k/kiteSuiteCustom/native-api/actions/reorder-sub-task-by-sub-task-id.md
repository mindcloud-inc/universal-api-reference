# Reorder sub task by sub task Id with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/task/sub-task/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Reorder sub task by sub task Id](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Sub Task ID |
| `position` | body | `string` | yes | — |
