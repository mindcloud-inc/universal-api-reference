# Check User In Team with Rollbar

Retrieves whether a user belongs to a Rollbar team.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/user/:userId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Check User In Team](https://docs.rollbar.com/reference/check-if-a-user-is-assigned-to-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
| `userId` | path | `number` | yes | Rollbar user identifier. |
