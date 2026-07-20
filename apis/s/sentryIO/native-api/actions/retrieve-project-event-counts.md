# Retrieve Project Event Counts with Sentry IO

Retrieves project event counts from Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:organization_id_or_slug/:project_id_or_slug/stats/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Project Event Counts](https://docs.sentry.io/api/projects/retrieve-event-counts-for-a-project/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `project_id_or_slug` | path | `string` | yes | The Sentry project ID or slug. |
