# Get Schedule Metadata with Procore

Retrieves schedule metadata from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/:project_id/schedule`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [Get Schedule Metadata](https://developers.procore.com/reference/rest/schedule#get-schedule-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
