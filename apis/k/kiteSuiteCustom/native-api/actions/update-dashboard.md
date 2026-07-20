# Update Dashboard with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/dashboard/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Dashboard](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | dashboardID |
| `body` | body | `object` | yes | Request body |
| `name` | body | `string` | yes | — |
| `privacy` | body | `string` | yes | — |
| `widgetName` | body | `string` | yes | — |
| `type` | body | `string` | yes | — |
| `project` | body | `string` | yes | — |
| `sprint` | body | `string` | yes | — |
| `lists[]` | body | `array` | yes | — |
| `estimateBy` | body | `string` | yes | — |
| `groupBy` | body | `string` | yes | — |
