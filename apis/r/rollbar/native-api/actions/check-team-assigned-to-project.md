# Check Team Assigned To Project with Rollbar

Retrieves whether a team is assigned to a Rollbar project.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:projectId/team/:teamId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Check Team Assigned To Project](https://docs.rollbar.com/reference/check-if-a-team-is-assigned-to-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier. |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
