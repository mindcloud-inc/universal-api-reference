# Create Task with Jostle

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks`
- **Base URL:** `https://api-prod.jostle.us`
- **Official documentation:** [Create Task](https://api.jostle.me/reference/posttask-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the task |
| `description` | body | `string` | no | Description of the task |
| `dueDate` | body | `string` | no | Task due date as an ISO 8601 datetime |
| `assignee.userId` | body | `string` | no | Id of the user assigned to the task |
| `assignee.username` | body | `string` | no | Username of the user assigned to the task |
| `collaborators.presetId` | body | `string` | no | Preset list used to define task collaborators |
