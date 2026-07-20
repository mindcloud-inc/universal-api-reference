# List Experiments with Galileo

Finds experiments for a Galileo project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/experiments`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [List Experiments](https://docs.galileo.ai/api-reference/experiment/list-experiments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
