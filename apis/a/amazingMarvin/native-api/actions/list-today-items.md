# List Today Items with Amazing Marvin

Retrieves today's scheduled items from Amazing Marvin.

## Endpoint

- **Method:** `GET`
- **Path:** `/todayItems`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [List Today Items](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-tasks-and-projects-scheduled-today-including-rolloverauto-schedule-due-items-if-enabled)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Date in YYYY-MM-DD format. |
