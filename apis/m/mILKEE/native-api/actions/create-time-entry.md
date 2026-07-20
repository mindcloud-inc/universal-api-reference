# Create Time Entry with MILKEE

Creates a new time entry in MILKEE.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/times`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Create Time Entry](https://apidocs.milkee.ch/api/resources/times.html#create-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable` | body | `boolean` | no | Whether the time is billable. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `date` | body | `string` | yes | Date of work. |
| `description` | body | `string` | no | Description of work performed. |
| `end` | body | `string` | no | End time in H:i format. |
| `hourly_rate` | body | `number` | no | Hourly rate for the entry. |
| `hours` | body | `number` | yes | Hours worked. |
| `minutes` | body | `number` | yes | Minutes worked. |
| `project_id` | body | `number` | yes | ID of the project. |
| `start` | body | `string` | no | Start time in H:i format. |
| `task_id` | body | `number` | no | Associated task ID. |
