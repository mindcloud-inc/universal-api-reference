# Get Experiment Results with Optimizely

Retrieves results for an experiment in Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments/{experimentId}/results`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [Get Experiment Results](https://docs.developers.optimizely.com/web-experimentation/reference/get_experiment_results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | The experiment id to fetch results for. |
