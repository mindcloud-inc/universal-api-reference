# Get Experiment with Galileo

Retrieves an experiment from Galileo by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/experiments/:experiment_id`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Experiment](https://docs.galileo.ai/api-reference/experiment/get-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | Galileo experiment UUID. |
| `project_id` | path | `string` | yes | Galileo project UUID. |
