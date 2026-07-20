# Create Task with Moxie

Creates a new task in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/tasks/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Task](https://help.withmoxie.com/en/articles/8160423-create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Task name. |
| `clientName` | body | `string` | yes | Existing client name for the task. |
| `projectName` | body | `string` | yes | Existing project name for the task. |
| `status` | body | `string` | no | Task status label. |
| `description` | body | `string` | no | Task description. |
| `dueDate` | body | `date` | no | Task due date. |
| `startDate` | body | `date` | no | Task start date. |
| `priority` | body | `number` | no | Task priority value. |
| `assignedTo` | body | `list<string>` | no | List of assignee emails. |
| `tasks` | body | `list<string>` | no | Optional list of subtask labels. |
| `customValues` | body | `object` | no | Custom values object for the task. |
