# List Team Tasks with Onfleet

Retrieves unassigned tasks for a team in Onfleet.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/tasks`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [List Team Tasks](https://docs.onfleet.com/reference/list-tasks-in-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The Onfleet team ID. |
