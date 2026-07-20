# Create Incident with Procore

Creates a new incident in Procore.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v1.0/projects/:project_id/incidents`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [Create Incident](https://developers.procore.com/reference/rest/incidents#create-incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident` | body | `object` | yes | Incident payload object. |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
