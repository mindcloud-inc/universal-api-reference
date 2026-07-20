# Create Task Comment with ProjectManager

Creates a new task comment in ProjectManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data/tasks/:taskId/comments`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Create Task Comment](https://developer.projectmanager.com/api-reference/discussion/create-task-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The unique ID number of the task being commented upon |
| `text` | body | `string` | no | The text of the comment to add to the discussion, in Markdown format.              Discussion comments are formatted using [Markdown](https://www.markdownguide.org/) and users should be aware that HTML embedding is not permitted due to the risk of cross-site attacks and other embedding challenges. |
