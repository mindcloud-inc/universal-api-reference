# Remove User From Team with Rollbar

Removes a user from a team in Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/team/:teamId/user/:userId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Remove User From Team](https://docs.rollbar.com/reference/remove-a-user-from-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
| `userId` | path | `number` | yes | Rollbar user identifier. |
