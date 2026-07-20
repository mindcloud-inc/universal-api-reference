# List Allocations with Float

Retrieves allocations from Float.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [List Allocations](https://developer.float.com/api_reference.html#Allocations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | A project ID to filter the response on |
| `people_id` | query | `number` | no | A people ID to filter the response on |
| `start_date` | query | `string` | no | Start of date range in format YYYY-MM-DD |
| `end_date` | query | `string` | no | End of date range in format YYYY-MM-DD |
| `status` | query | `number` | no | Filter response on the allocation status |
| `modified_since` | query | `string` | no | Filter on records with an equal or later modified timestamp |
| `fields` | query | `string` | no | Comma-delimited set of fields to include in the response |
| `expand` | query | `string` | no | Use task_days to return additional calculated dates for each allocation |
