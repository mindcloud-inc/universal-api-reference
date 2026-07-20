# Create Project with Amazing Marvin

Creates a project in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/addProject`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Create Project](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Project title. |
| `day` | body | `string` | no | Schedule date in YYYY-MM-DD format or null. |
| `priority` | body | `string` | no | low, mid, or high. |
| `parentId` | body | `string` | no | Optional parent category or project ID. |
| `dueDate` | body | `string` | no | Due date in YYYY-MM-DD format. |
| `timeZoneOffset` | body | `number` | no | Timezone offset in minutes. |
