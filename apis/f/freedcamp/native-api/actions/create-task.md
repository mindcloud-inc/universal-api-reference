# Create Task with Freedcamp

Creates a new task in Freedcamp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks`
- **Base URL:** `https://freedcamp.com`
- **Official documentation:** [Create Task](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | The target Freedcamp project ID. |
| `title` | body | `string` | yes | The task title. |
| `description` | body | `string` | no | Optional task description. |
