# List User Projects with Rollbar

Retrieves projects for a Rollbar user.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:userId/projects`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List User Projects](https://docs.rollbar.com/reference/list-a-users-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | Rollbar user identifier. |
