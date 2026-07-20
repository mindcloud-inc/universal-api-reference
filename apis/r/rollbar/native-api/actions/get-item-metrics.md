# Get Item Metrics with Rollbar

Retrieves item metrics from Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/metrics/items`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Item Metrics](https://docs.rollbar.com/reference/post_api-1-metrics-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_counters` | body | `string` | yes | List of Rollbar item counters |
