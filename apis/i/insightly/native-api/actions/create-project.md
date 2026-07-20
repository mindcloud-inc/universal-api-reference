# Create Project with Insightly

Creates a new project in Insightly.

## Endpoint

- **Method:** `POST`
- **Path:** `{apiBaseUrl}Projects`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Create Project](https://api.insightly.com/v3.1/Help#!/Projects/AddEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PROJECT_NAME` | body | `string` | yes | The project name. |
| `STATUS` | body | `string` | yes | The project status. |
| `PROJECT_DETAILS` | body | `string` | no | Details for the project. |
| `STARTED_DATE` | body | `string` | no | The project start date. |
| `COMPLETED_DATE` | body | `string` | no | The project completion date. |
