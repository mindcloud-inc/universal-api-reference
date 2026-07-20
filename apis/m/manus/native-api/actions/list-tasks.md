# List Tasks with Manus

Retrieves tasks from Manus with optional filtering and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.manus.ai/v1`
- **Official documentation:** [List Tasks](https://open.manus.ai/docs/v1/get-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search keyword for tasks |
| `created_after` | query | `number` | no | Return tasks created after the given Unix timestamp in milliseconds |
| `created_before` | query | `number` | no | Return tasks created before the given Unix timestamp in milliseconds |
| `project_id` | query | `string` | no | Filter tasks by project ID |
