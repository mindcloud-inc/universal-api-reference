# Assign User To Team with Rollbar

Assigns a user to a team in Rollbar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/team/:teamId/user/:userId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Assign User To Team](https://docs.rollbar.com/reference/assign-a-user-to-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | Rollbar team identifier. |
| `userId` | path | `number` | yes | Rollbar user identifier. |
