# Get Analytics Raw Hits with redirect.pizza

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/analytics/raw`
- **Base URL:** `https://redirect.pizza`
- **Official documentation:** [Get Analytics Raw Hits](https://redirect.pizza/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | no | Start date or timestamp for the analytics window. |
| `end` | query | `string` | no | End date or timestamp for the analytics window. |
| `query` | query | `string` | no | Filter expression for analytics results. |
| `cursor` | query | `string` | no | Cursor token for the next page of raw analytics results. |
