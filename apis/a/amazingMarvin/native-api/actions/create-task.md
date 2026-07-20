# Create Task with Amazing Marvin

Creates a task in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/addTask`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Create Task](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Task title. |
| `day` | body | `string` | no | Schedule date in YYYY-MM-DD format. |
| `dueDate` | body | `string` | no | Due date in YYYY-MM-DD format. |
| `parentId` | body | `string` | no | Optional parent category or project ID. |
| `timeZoneOffset` | body | `number` | no | Timezone offset in minutes. |
