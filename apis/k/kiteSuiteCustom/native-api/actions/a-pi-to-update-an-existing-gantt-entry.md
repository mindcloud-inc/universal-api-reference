# API to update an existing Gantt entry with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/gantt/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [API to update an existing Gantt entry](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Gantt entry ID |
| `title` | body | `string` | yes | — |
| `isEnable` | body | `boolean` | yes | — |
| `view` | body | `string` | yes | — |
