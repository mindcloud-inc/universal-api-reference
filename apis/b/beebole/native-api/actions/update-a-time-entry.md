# Update a Time Entry with Beebole

Updates an existing time entry in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Update a Time Entry](https://beebole.com/help/api#update-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | The Beebole time entry identifier. |
| `company.id` | body | `number` | no | Optional company identifier when moving a time entry to a company-level target. |
| `project.id` | body | `number` | no | Optional project identifier when moving a time entry to a project-level target. |
| `subproject.id` | body | `number` | no | Optional subproject identifier when moving a time entry to a subproject-level target. |
| `absence.id` | body | `number` | no | Optional absence identifier when converting a time entry to an absence entry. |
| `task.id` | body | `number` | no | Optional task identifier. Required when tasks exist for the selected entity and the entry is not an absence. |
| `date` | body | `string` | yes | The time entry date in YYYY-MM-DD format. |
| `hours` | body | `number` | yes | The number of hours to store on the time entry. |
| `comment` | body | `string` | no | Optional comment stored on the time entry. |
