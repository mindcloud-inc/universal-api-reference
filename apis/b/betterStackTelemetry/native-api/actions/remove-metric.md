# Remove Metric with Better Stack Telemetry

Deletes an existing metric from Better Stack Telemetry.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/sources/:source_id/metrics/:id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Remove Metric](https://betterstack.com/docs/logs/api/deleting-an-existing-metric/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Source for which to delete a metric |
| `id` | path | `string` | yes | ID of the metric to delete |
