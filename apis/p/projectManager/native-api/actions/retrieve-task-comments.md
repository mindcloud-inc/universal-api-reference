# Retrieve Task Comments with ProjectManager

Retrieves task comments from ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/tasks/:taskId/comments`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Retrieve Task Comments](https://developer.projectmanager.com/api-reference/discussion/retrieve-task-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The unique ID number of the task to retrieve comments |
