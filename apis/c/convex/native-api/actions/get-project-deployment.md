# Get Project Deployment with Convex

Retrieves a deployment from a Convex project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/deployment`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Get Project Deployment](https://docs.convex.dev/management-api/get-deployment-in-project-by-project-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Convex project ID. |
| `reference` | query | `string` | no | The deployment reference to fetch. |
| `defaultProd` | query | `boolean` | no | Fetch the default production deployment for the caller. |
| `defaultDev` | query | `boolean` | no | Fetch the default development deployment for the caller. |
