# Assign Team To Project with Rollbar

Assigns a team to a project in Rollbar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project/:projectId/team/:teamId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Assign Team To Project](https://docs.rollbar.com/reference/assign-a-team-to-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier. |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
