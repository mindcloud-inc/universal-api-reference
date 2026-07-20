# Create Task with Everhour

Creates a new task in Everhour.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/tasks`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Create Task](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Everhour project ID. |
| `name` | body | `string` | yes | Task name. |
| `section` | body | `number` | yes | Section ID within the project. |
| `labels[]` | body | `array<string>` | no | Task labels. |
| `position` | body | `number` | no | Task position in the section. |
| `description` | body | `string` | no | Task description. |
| `dueOn` | body | `string` | no | Due date in YYYY-MM-DD format. |
| `status` | body | `string` | no | Task status. |
