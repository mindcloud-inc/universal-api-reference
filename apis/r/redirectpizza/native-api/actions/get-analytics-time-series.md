# Get Analytics Time Series with redirect.pizza

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/analytics/time-series`
- **Base URL:** `https://redirect.pizza`
- **Official documentation:** [Get Analytics Time Series](https://redirect.pizza/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | no | Start date or timestamp for the analytics window. |
| `end` | query | `string` | no | End date or timestamp for the analytics window. |
| `query` | query | `string` | no | Filter expression for analytics results. |
