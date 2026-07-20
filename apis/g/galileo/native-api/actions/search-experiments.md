# Search Experiments with Galileo

Finds experiments in a Galileo project by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects/:project_id/experiments/search`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Search Experiments](https://docs.galileo.ai/api-reference/experiment/search-experiments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Galileo project UUID. |
