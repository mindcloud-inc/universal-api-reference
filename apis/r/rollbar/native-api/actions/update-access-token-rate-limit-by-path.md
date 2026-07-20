# Update Access Token Rate Limit By Path with Rollbar

Updates a project access token rate limit in Rollbar by path identifier.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/project/:projectId/access_token/:tokenIdentifier`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Update Access Token Rate Limit By Path](https://docs.rollbar.com/reference/update-a-rate-limit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier |
| `tokenIdentifier` | path | `string` | yes | Project access token identifier |
