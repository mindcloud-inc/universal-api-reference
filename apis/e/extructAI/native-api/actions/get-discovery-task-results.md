# Get Discovery Task Results with Extruct AI

Retrieves discovery task results from Extruct AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/discovery_tasks/:task_id/results`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Get Discovery Task Results](https://docs.extruct.ai/api-reference/discover/get-company-discovery-task-results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Deep Search task identifier. |
