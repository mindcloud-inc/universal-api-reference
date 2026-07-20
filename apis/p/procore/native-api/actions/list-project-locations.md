# List Project Locations with Procore

Retrieves project locations from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/:project_id/locations`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Project Locations](https://developers.procore.com/reference/rest/locations#list-project-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
