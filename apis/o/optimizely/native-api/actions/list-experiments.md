# List Experiments with Optimizely

Retrieves a list of experiments from Optimizely.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [List Experiments](https://docs.developers.optimizely.com/web-experimentation/reference/list_experiments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | Filter experiments to one project. |
