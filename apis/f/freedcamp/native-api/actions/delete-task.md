# Delete Task with Freedcamp

Deletes an existing task from Freedcamp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/tasks/:taskId`
- **Base URL:** `https://freedcamp.com`
- **Official documentation:** [Delete Task](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The Freedcamp task ID. |
