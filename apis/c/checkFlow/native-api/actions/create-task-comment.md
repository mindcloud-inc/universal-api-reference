# Create Task Comment with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/task/comment`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Create Task Comment](https://docs.checkflow.io/docs/api/tasks#create-task-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskID` | body | `number` | yes | The ID of the task to comment on. |
| `commentHtml` | body | `string` | yes | The comment content as an HTML string. |
| `createdByUserID` | body | `number` | yes | The ID of the user creating the comment. Use 0 for anonymous. |
