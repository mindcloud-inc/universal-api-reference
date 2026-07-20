# List Activity Log with PostHog

Retrieves activity log entries from a PostHog project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/activity_log/`
- **Base URL:** `https://us.posthog.com/api`
- **Official documentation:** [List Activity Log](https://posthog.com/docs/api/activity-log)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
