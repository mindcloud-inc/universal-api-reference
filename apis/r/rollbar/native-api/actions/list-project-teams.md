# List Project Teams with Rollbar

Retrieves teams for a Rollbar project.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:projectId/teams`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List Project Teams](https://docs.rollbar.com/reference/list-a-projects-teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier. |
