# Create Project with ArcSite

Creates a new project in ArcSite.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Create Project](https://dev.arcsite.com/#create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_number` | body | `string` | no | Job number of the project. |
| `name` | body | `string` | yes | Name of the project. |
| `owner` | body | `string` | yes | Valid ArcSite username or email that owns the project. |
