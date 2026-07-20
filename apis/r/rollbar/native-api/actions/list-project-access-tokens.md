# List Project Access Tokens with Rollbar

Retrieves project access tokens from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:projectId/access_tokens`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List Project Access Tokens](https://docs.rollbar.com/reference/list-all-project-access-tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier. |
