# List Schedules with Procore

Retrieves schedules from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2.0/companies/:company_id/projects/:project_id/schedules`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Schedules](https://developers.procore.com/reference/rest/schedules#list-schedules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Unique identifier for the company. |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
