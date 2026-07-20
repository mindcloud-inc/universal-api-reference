# Delete Project Access Token By Body with Rollbar

Deletes a project access token from Rollbar by body identifier.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:projectId/access_token`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Project Access Token By Body](https://docs.rollbar.com/reference/delete-a-project-access-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier |
