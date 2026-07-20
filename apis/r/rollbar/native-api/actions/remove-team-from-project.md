# Remove Team From Project with Rollbar

Removes a team from a project in Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:projectId/team/:teamId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Remove Team From Project](https://docs.rollbar.com/reference/remove-a-team-from-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier. |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
