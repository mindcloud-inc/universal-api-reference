# List Team Deployments with Convex

Retrieves deployments from a Convex team.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team_id/list_deployments`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [List Team Deployments](https://docs.convex.dev/management-api/list-deployments-for-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `number` | yes | The Convex team ID. |
