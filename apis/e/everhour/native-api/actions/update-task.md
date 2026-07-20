# Update Task with Everhour

Updates an existing task in Everhour.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Update Task](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Everhour task ID. |
| `name` | body | `string` | yes | Task name. |
| `section` | body | `number` | yes | Section ID within the project. |
| `labels[]` | body | `array<string>` | no | Task labels. |
| `position` | body | `number` | no | Task position in the section. |
| `description` | body | `string` | no | Task description. |
| `dueOn` | body | `string` | no | Due date in YYYY-MM-DD format. |
| `status` | body | `string` | no | Task status. |
