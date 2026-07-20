# Create an Experiment with Arize AX

Creates a new experiment in Arize AX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/experiments`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Create an Experiment](https://arize.com/docs/api-reference/experiments/create-an-experiment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dataset_id` | body | `string` | yes |
| `experiment_runs[]` | body | `array<object>` | yes |
| `name` | body | `string` | yes |
