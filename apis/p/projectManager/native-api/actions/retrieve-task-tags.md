# Retrieve TaskTags with ProjectManager

Retrieves task tags from ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/tasks/:taskId/tags`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Retrieve TaskTags](https://developer.projectmanager.com/api-reference/task-tag/retrieve-task-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The unique identifier of the Task for which we will retrieve TaskTags |
