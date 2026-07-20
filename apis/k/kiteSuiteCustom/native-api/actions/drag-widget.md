# drag widget with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/dashboard/drag-widget/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [drag widget](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | dashboardID |
| `body` | body | `object` | yes | Request body |
| `widgetId` | body | `string` | yes | — |
| `position` | body | `number` | yes | — |
