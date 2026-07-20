# Get Project By Slug with Convex

Retrieves a project from Convex by slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team_id_or_slug/projects/:project_slug`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Get Project By Slug](https://docs.convex.dev/management-api/get-project-by-slug)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id_or_slug` | path | `string` | yes | The Convex team ID or slug. |
| `project_slug` | path | `string` | yes | The Convex project slug. |
