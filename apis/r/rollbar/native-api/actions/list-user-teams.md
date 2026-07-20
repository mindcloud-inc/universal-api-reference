# List User Teams with Rollbar

Retrieves teams for a Rollbar user.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:userId/teams`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List User Teams](https://docs.rollbar.com/reference/list-a-users-teams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | Rollbar user identifier. |
