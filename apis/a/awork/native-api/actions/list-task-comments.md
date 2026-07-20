# List Task Comments with Awork

Retrieves task comments from Awork.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId/comments`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [List Task Comments](https://developers.awork.com/apiv1/task-comments/get-task-comments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The id of the task. |
