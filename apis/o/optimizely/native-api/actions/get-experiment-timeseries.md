# Get Experiment Timeseries with Optimizely

Retrieves experiment time series from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments/{experimentId}/timeseries`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [Get Experiment Timeseries](https://docs.developers.optimizely.com/web-experimentation/reference/get_experiment_timeseries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | The experiment id to fetch timeseries for. |
