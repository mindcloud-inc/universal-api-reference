# Convex: Native API Reference

A consolidated summary of Convex's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.convex.dev/management-api
- **OpenAPI specification:** https://api.convex.dev/v1/openapi.json
- **API base URL:** `https://api.convex.dev/v1`

## Authentication

### Bearer Token

Use a Convex team access token in the Authorization header for Management API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.convex.dev/management-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Deployment](actions/create-deployment.md) | `POST /projects/:project_id/create_deployment` | [docs](https://docs.convex.dev/management-api/create-deployment) |
| [Create Project](actions/create-project.md) | `POST /teams/:team_id/create_project` | [docs](https://docs.convex.dev/management-api/create-project) |
| [Delete Deployment](actions/delete-deployment.md) | `POST /deployments/:deployment_name/delete` | [docs](https://docs.convex.dev/management-api/delete-deployment) |
| [Delete Project](actions/delete-project.md) | `POST /projects/:project_id/delete` | [docs](https://docs.convex.dev/management-api/delete-project) |
| [Get Deployment](actions/get-deployment.md) | `GET /deployments/:deployment_name` | [docs](https://docs.convex.dev/management-api/platform-get-deployment) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://docs.convex.dev/management-api/get-project-by-id) |
| [Get Project By Slug](actions/get-project-by-slug.md) | `GET /teams/:team_id_or_slug/projects/:project_slug` | [docs](https://docs.convex.dev/management-api/get-project-by-slug) |
| [Get Project Deployment](actions/get-project-deployment.md) | `GET /projects/:project_id/deployment` | [docs](https://docs.convex.dev/management-api/get-deployment-in-project-by-project-id) |
| [Get Project Deployment By Slug](actions/get-project-deployment-by-slug.md) | `GET /teams/:team_id_or_slug/projects/:project_slug/deployment` | [docs](https://docs.convex.dev/management-api/get-deployment-in-project-by-project-slug) |
| [Get Token Details](actions/get-token-details.md) | `GET /token_details` | [docs](https://docs.convex.dev/management-api/get-token-details) |
| [List Default Environment Variables](actions/list-default-environment-variables.md) | `GET /projects/:project_id/list_default_environment_variables` | [docs](https://docs.convex.dev/production/environment-variables) |
| [List Deployment Classes](actions/list-deployment-classes.md) | `GET /teams/:team_id/list_deployment_classes` | [docs](https://docs.convex.dev/management-api/list-deployment-classes) |
| [List Deployment Regions](actions/list-deployment-regions.md) | `GET /teams/:team_id/list_deployment_regions` | [docs](https://docs.convex.dev/management-api/list-deployment-regions) |
| [List Local Deployments](actions/list-local-deployments.md) | `GET /teams/:team_id/list_local_deployments` | [docs](https://docs.convex.dev/management-api/list-local-deployments-for-team) |
| [List Preview Deploy Keys](actions/list-preview-deploy-keys.md) | `GET /projects/:project_id/list_preview_deploy_keys` | [docs](https://docs.convex.dev/management-api/list-preview-deploy-keys) |
| [List Project Deployments](actions/list-project-deployments.md) | `GET /projects/:project_id/list_deployments` | [docs](https://docs.convex.dev/management-api/list-deployments) |
| [List Projects](actions/list-projects.md) | `GET /teams/:team_id/list_projects` | [docs](https://docs.convex.dev/management-api/list-projects) |
| [List Team Deployments](actions/list-team-deployments.md) | `GET /teams/:team_id/list_deployments` | [docs](https://docs.convex.dev/management-api/list-deployments-for-team) |
| [Update Default Environment Variables](actions/update-default-environment-variables.md) | `POST /projects/:project_id/update_default_environment_variables` | [docs](https://docs.convex.dev/production/environment-variables) |
| [Update Deployment](actions/update-deployment.md) | `PATCH /deployments/:deployment_name` | [docs](https://docs.convex.dev/management-api/update-deployment) |
