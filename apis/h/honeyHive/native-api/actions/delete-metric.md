# Delete Metric with HoneyHive

Deletes an existing metric from HoneyHive.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/metrics`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Delete Metric](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metric_id` | query | `string` | yes | Metric ID to delete. |
