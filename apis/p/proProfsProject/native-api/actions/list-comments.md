# List Comments with ProProfs Project

Retrieves a list of comments from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Comments](https://help.proprofsproject.com/managing-comments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Limit the number of returned comments. |
| `offset` | query | `string` | no | Offset for returned comments. |
| `project_id` | query | `string` | no | Filter comments by project ID. |
| `subtask_id` | query | `string` | no | Filter comments by subtask ID. |
| `task_id` | query | `string` | no | Filter comments by task ID. |
