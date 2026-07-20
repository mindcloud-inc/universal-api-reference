# List Experiments Paginated with Galileo

Finds experiments for a Galileo project with pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/experiments/paginated`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [List Experiments Paginated](https://docs.galileo.ai/api-reference/experiment/list-experiments-paginated)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
