# Create Project Access Token with Rollbar

Creates a new project access token in Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:projectId/access_tokens`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Create Project Access Token](https://docs.rollbar.com/reference/post_api-1-project-project-id-access-tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name to identify the access token. |
| `projectId` | path | `number` | yes | Rollbar project identifier. |
| `scopes` | body | `string<string>` | yes | Scopes to assign to the access token. Send multiple values as a array. |
