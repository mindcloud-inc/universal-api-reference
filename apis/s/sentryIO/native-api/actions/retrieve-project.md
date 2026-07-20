# Retrieve Project with Sentry IO

Retrieves a project from Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:organization_id_or_slug/:project_id_or_slug/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Project](https://docs.sentry.io/api/projects/retrieve-a-project/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `project_id_or_slug` | path | `string` | yes | The Sentry project ID or slug. |
