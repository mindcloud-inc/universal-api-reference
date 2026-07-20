# Get Experiment Result with HoneyHive

Retrieves an experiment result from HoneyHive.

## Endpoint

- **Method:** `GET`
- **Path:** `/runs/{run_id}/result`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Get Experiment Result](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | Run ID. |
| `project_id` | query | `string` | yes | Project ID. |
| `aggregate_function` | query | `string` | no | Aggregate function. |
