# List Section Tasks with OneSuite

Retrieves tasks for a project section in OneSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/sections/:section_id/tasks`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [List Section Tasks](https://rest-api.onesuite.io/#get-all-tasks-of-section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The ID of the project |
| `section_id` | path | `string` | yes | The ID of the section |
