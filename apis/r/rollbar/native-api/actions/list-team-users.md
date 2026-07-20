# List Team Users with Rollbar

Retrieves users assigned to a Rollbar team.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/users`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List Team Users](https://docs.rollbar.com/reference/list-a-teams-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
