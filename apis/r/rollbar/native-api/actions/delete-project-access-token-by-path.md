# Delete Project Access Token By Path with Rollbar

Deletes a project access token from Rollbar by path identifier.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:projectId/access_token/:tokenIdentifier`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Project Access Token By Path](https://docs.rollbar.com/reference/delete-a-project-access-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier |
| `tokenIdentifier` | path | `string` | yes | Project access token identifier |
