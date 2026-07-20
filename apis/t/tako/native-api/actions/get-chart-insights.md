# Get Chart Insights with Tako

Retrieves insights from a Tako knowledge card chart.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/beta/chart_insights`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Get Chart Insights](https://docs.tako.com/api-reference/insights)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card_id` | query | `string` | yes | ID of the chart knowledge card to inspect. |
