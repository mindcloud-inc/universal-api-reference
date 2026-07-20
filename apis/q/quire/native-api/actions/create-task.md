# Create Task with Quire

Creates a new task in Quire.

## Endpoint

- **Method:** `POST`
- **Path:** `task/id/:projectId`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Create Task](https://quire.io/dev/api/#operation--task-id--projectId--post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID or shortcut, for example App_Account. |
| `name` | body | `string` | yes | The title of the new task. |
| `description` | body | `string` | no | Optional task description in Markdown. |
