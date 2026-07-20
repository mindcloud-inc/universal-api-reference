# List Project Error Events with Sentry IO

Retrieves error events from a Sentry IO project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:organization_id_or_slug/:project_id_or_slug/events/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Project Error Events](https://docs.sentry.io/api/events/list-a-projects-error-events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `project_id_or_slug` | path | `string` | yes | The Sentry project ID or slug. |
