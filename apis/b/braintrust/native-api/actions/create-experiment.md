# Create Experiment with Braintrust

Creates a new experiment in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/experiment`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Create Experiment](https://www.braintrust.dev/docs/api-reference/experiments/create-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project id. |
| `name` | body | `string` | no | Experiment name. |
