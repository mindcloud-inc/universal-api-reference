# Get Experiment Metrics with Galileo

Retrieves metrics for a Galileo experiment.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects/:project_id/experiments/:experiment_id/metrics`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Experiment Metrics](https://docs.galileo.ai/api-reference/trends-dashboard/get-experiment-metrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | Galileo experiment UUID. |
| `project_id` | path | `string` | yes | Galileo project UUID. |
