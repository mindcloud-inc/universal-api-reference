# List Task Comments with Runrun.it

Retrieves comments for a task in Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:task_id/comments`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Task Comments](https://runrun.it/api/documentation#comments-list-comments-on-a-task)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Task Id path parameter. |
