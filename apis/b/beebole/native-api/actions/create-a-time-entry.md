# Create a Time Entry with Beebole

Creates a new time entry in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Create a Time Entry](https://beebole.com/help/api#create-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company.id` | body | `number` | no | Optional company identifier when creating a company-level time entry. |
| `project.id` | body | `number` | no | Optional project identifier when creating a project-level time entry. |
| `subproject.id` | body | `number` | no | Optional subproject identifier when creating a subproject-level time entry. |
| `absence.id` | body | `number` | no | Optional absence identifier when creating an absence time entry. |
| `task.id` | body | `number` | no | Optional task identifier. Required when tasks exist for the selected entity and the entry is not an absence. |
| `date` | body | `string` | yes | The work date for the time entry in YYYY-MM-DD format. |
| `hours` | body | `number` | yes | The number of hours to log. |
| `comment` | body | `string` | no | Optional comment stored on the time entry. |
