# Get metric usage across experiments with GrowthBook

Retrieves metric usage across GrowthBook experiments.

## Endpoint

- **Method:** `GET`
- **Path:** `/usage/metrics`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get metric usage across experiments](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | List of comma-separated metric IDs (both fact and legacy) to get usage for, e.g. ids=met_123,fact_456 |
