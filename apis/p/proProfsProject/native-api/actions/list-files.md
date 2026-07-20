# List Files with ProProfs Project

Retrieves a list of files from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Files](https://help.proprofsproject.com/files)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Limit the number of returned files. |
| `offset` | query | `string` | no | Offset for returned files. |
| `order` | query | `string` | no | Sort order for returned files. |
| `project_id` | query | `string` | no | Filter files by project. |
| `subtask_id` | query | `string` | no | Filter files by subtask. |
| `task_id` | query | `string` | no | Filter files by task. |
