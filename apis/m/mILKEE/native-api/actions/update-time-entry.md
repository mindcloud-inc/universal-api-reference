# Update Time Entry with MILKEE

Updates an existing time entry in MILKEE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:companyId/times/:timeId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Time Entry](https://apidocs.milkee.ch/api/resources/times.html#update-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable` | body | `boolean` | no | Whether the time is billable. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `date` | body | `string` | no | Date of work. |
| `description` | body | `string` | no | Description of work performed. |
| `end` | body | `string` | no | End time in H:i format. |
| `force` | body | `boolean` | no | Force update of invoiced entries. |
| `hourly_rate` | body | `number` | no | Hourly rate for the entry. |
| `hours` | body | `number` | no | Hours worked. |
| `invoice_id` | body | `number` | no | Associated invoice ID. |
| `minutes` | body | `number` | no | Minutes worked. |
| `project_id` | body | `number` | no | ID of the project. |
| `start` | body | `string` | no | Start time in H:i format. |
| `status` | body | `string` | no | Time entry status: open, invoiced, or paid. |
| `task_id` | body | `number` | no | Associated task ID. |
| `time_id` | path | `string` | yes | The numeric MILKEE time entry ID used in the request path. |
