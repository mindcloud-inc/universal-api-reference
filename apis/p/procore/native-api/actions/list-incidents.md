# List Incidents with Procore

Retrieves incidents from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/:project_id/incidents`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Incidents](https://developers.procore.com/reference/rest/incidents#list-incidents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
