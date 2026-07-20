# Get Experiment Metric Settings with Galileo

Retrieves metric settings for a Galileo experiment.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/experiments/:experiment_id/metric_settings`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Experiment Metric Settings](https://docs.galileo.ai/api-reference/experiment/get-metric-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | Galileo experiment UUID. |
| `project_id` | path | `string` | yes | Galileo project UUID. |
