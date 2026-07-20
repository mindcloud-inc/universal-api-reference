# Update Access Token Rate Limit By Body with Rollbar

Updates a project access token rate limit in Rollbar by body identifier.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/project/:projectId/access_token`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Update Access Token Rate Limit By Body](https://docs.rollbar.com/reference/update-a-rate-limit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Rollbar project identifier |
