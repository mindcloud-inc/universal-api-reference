# Get Project Deployment By Slug with Convex

Retrieves a deployment from Convex by project slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team_id_or_slug/projects/:project_slug/deployment`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Get Project Deployment By Slug](https://docs.convex.dev/management-api/get-deployment-in-project-by-project-slug)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id_or_slug` | path | `string` | yes | The Convex team ID or slug. |
| `project_slug` | path | `string` | yes | The Convex project slug. |
| `reference` | query | `string` | no | The deployment reference to fetch. |
| `defaultProd` | query | `boolean` | no | Fetch the default production deployment for the caller. |
| `defaultDev` | query | `boolean` | no | Fetch the default development deployment for the caller. |
