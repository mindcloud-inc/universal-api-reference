# Create Comment with Freedcamp

Creates a new task comment in Freedcamp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/comments`
- **Base URL:** `https://freedcamp.com`
- **Official documentation:** [Create Comment](https://freedcamp.com/help_/tutorials/wiki/wiki_public/view/DFaab)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | yes | The target Freedcamp task ID. |
| `description` | body | `string` | yes | The comment body. |
