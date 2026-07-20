# Get Session Recording with PostHog

Retrieves a session recording from a PostHog project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/session_recordings/:id/`
- **Base URL:** `https://us.posthog.com/api`
- **Official documentation:** [Get Session Recording](https://posthog.com/docs/api/session-recordings)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | path | `string` | yes |
