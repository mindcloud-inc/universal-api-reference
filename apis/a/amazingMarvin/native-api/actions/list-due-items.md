# List Due Items with Amazing Marvin

Retrieves open due tasks and projects from Amazing Marvin.

## Endpoint

- **Method:** `GET`
- **Path:** `/dueItems`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [List Due Items](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-open-tasks-and-projects-that-are-due-today-or-earlier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `by` | query | `string` | no | Date in YYYY-MM-DD format. |
