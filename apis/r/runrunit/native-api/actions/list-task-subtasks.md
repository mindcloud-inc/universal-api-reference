# List Task Subtasks with Runrun.it

Retrieves subtasks for a task in Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:id/subtasks`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Task Subtasks](https://runrun.it/api/documentation#tasks-show-task-subtasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
