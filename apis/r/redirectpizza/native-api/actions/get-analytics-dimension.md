# Get Analytics Dimension with redirect.pizza

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/analytics/dimensions/{dimension}`
- **Base URL:** `https://redirect.pizza`
- **Official documentation:** [Get Analytics Dimension](https://redirect.pizza/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimension` | path | `string` | yes | Analytics dimension to group by. |
| `start` | query | `string` | no | Start date or timestamp for the analytics window. |
| `end` | query | `string` | no | End date or timestamp for the analytics window. |
| `query` | query | `string` | no | Filter expression for analytics results. |
