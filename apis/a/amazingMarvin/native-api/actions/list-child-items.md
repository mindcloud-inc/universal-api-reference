# List Child Items with Amazing Marvin

Retrieves open child tasks and projects from Amazing Marvin.

## Endpoint

- **Method:** `GET`
- **Path:** `/children`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [List Child Items](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-child-tasksprojects-of-a-categoryproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentId` | query | `string` | yes | Parent ID, or use unassigned for inbox items. |
