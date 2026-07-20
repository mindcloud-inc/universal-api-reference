# Update Project with Insightly

Updates an existing project in Insightly.

## Endpoint

- **Method:** `PUT`
- **Path:** `{apiBaseUrl}Projects`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Update Project](https://api.insightly.com/v3.1/Help#!/Projects/UpdateEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PROJECT_ID` | body | `number` | yes | The Project ID to update. |
| `PROJECT_NAME` | body | `string` | yes | The project name. |
| `STATUS` | body | `string` | yes | The project status. |
| `PROJECT_DETAILS` | body | `string` | no | Details for the project. |
| `STARTED_DATE` | body | `string` | no | The project start date. |
| `COMPLETED_DATE` | body | `string` | no | The project completion date. |
