# Create Metric with Better Stack Telemetry

Creates a new metric in Better Stack Telemetry.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/sources/:source_id/metrics`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Create Metric](https://betterstack.com/docs/logs/api/creating-a-metric/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Source for which to create a metric |
| `name` | body | `string` | yes | Metric name |
| `sql_expression` | body | `string` | yes | SQL expression to use for the metric |
| `team_name` | body | `string` | no | Required if using a global API token to specify the team that should own the metric |
| `aggregations[]` | body | `array<string>` | no | Aggregations to apply to the metric |
| `type` | body | `string` | no | Metric type |
