# List Team Projects with Rollbar

Retrieves projects for a Rollbar team.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List Team Projects](https://docs.rollbar.com/reference/list-a-teams-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
