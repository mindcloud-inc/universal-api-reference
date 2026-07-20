# List Session Recordings with PostHog

Retrieves session recordings from a PostHog project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/session_recordings/`
- **Base URL:** `https://us.posthog.com/api`
- **Official documentation:** [List Session Recordings](https://posthog.com/docs/api/session-recordings)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `string` | no |
| `project_id` | path | `string` | yes |
| `offset` | query | `string` | no |
