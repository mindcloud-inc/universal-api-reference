# List Project Users with Sentry IO

Retrieves users from a Sentry IO project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:organization_id_or_slug/:project_id_or_slug/users/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Project Users](https://docs.sentry.io/api/projects/list-a-projects-users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `project_id_or_slug` | path | `string` | yes | The Sentry project ID or slug. |
