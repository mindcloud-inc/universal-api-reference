# List Sections with Optimizely

Retrieves sections for an experiment in Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments/{experimentId}/sections`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Sections](https://docs.developers.optimizely.com/web-experimentation/reference/get_experiment_sections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experiment_id` | path | `string` | yes | The multivariate experiment id. |
