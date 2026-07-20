# update widget with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/dashboard/widget/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [update widget](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | widgetID |
| `body` | body | `object` | yes | Request body |
| `project` | body | `string` | yes | — |
| `widgetName` | body | `string` | yes | — |
| `groupBy` | body | `string` | yes | — |
| `type` | body | `string` | yes | — |
