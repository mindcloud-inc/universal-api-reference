# List Logged Time with Float

Retrieves logged time entries from Float.

## Endpoint

- **Method:** `GET`
- **Path:** `/logged-time`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [List Logged Time](https://developer.float.com/api_reference.html#Logged_Time)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | End of date range in format YYYY-MM-DD |
| `fields` | query | `string` | no | Comma-delimited set of fields to include in the response |
| `modified_since` | query | `string` | no | Filter on records with an equal or later modified timestamp |
| `people_id` | query | `number` | no | A people ID to filter the response on |
| `phase_id` | query | `string` | no | A phase ID associated with a project to filter the response on |
| `start_date` | query | `string` | no | Start of date range in format YYYY-MM-DD |
| `task_meta_id` | query | `string` | no | A project task ID to filter the response on |
| `project_id` | query | `number` | no | A project ID to filter the response on |
| `phase_id` | query | `number` | no | A phase ID associated with a project to filter the response on |
| `task_meta_id` | query | `number` | no | A project task ID to filter the response on |
| `start_date` | query | `string` | no | Start of date range in format YYYY-MM-DD |
| `end_date` | query | `string` | no | End of date range in format YYYY-MM-DD |
| `modified_since` | query | `string` | no | Filter on records with an equal or later modified timestamp |
| `fields` | query | `string` | no | Comma-delimited set of fields to include in the response |
