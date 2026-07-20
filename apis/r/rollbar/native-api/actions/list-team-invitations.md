# List Team Invitations with Rollbar

Retrieves team invitations from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/invites`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List Team Invitations](https://docs.rollbar.com/reference/list-invitations-for-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | Rollbar team identifier |
