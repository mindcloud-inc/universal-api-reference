# Delete Project with Rollbar

Deletes an existing project from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:projectId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Project](https://docs.rollbar.com/reference/delete-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier. |
