# Get Experiment Comparison with HoneyHive

Retrieves an experiment comparison from HoneyHive.

## Endpoint

- **Method:** `GET`
- **Path:** `/runs/{run_id_1}/compare-with/{run_id_2}`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Get Experiment Comparison](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id_1` | path | `string` | yes | First run ID. |
| `run_id_2` | path | `string` | yes | Second run ID. |
| `project_id` | query | `string` | yes | Project ID. |
| `aggregate_function` | query | `string` | no | Aggregate function. |
