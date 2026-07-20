# List Schedule Activities with Procore

Retrieves schedule activities from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2.0/companies/:company_id/projects/:project_id/schedules/:schedule_id/activities`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Schedule Activities](https://developers.procore.com/reference/rest/activities#list-activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique identifier for the company. |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
| `schedule_id` | path | `string` | yes | Unique identifier for the schedule. |
