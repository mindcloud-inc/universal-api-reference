# <img src="https://images.mindcloud.co/apps/icons/9a72d8f2-e4a4-406d-ad12-ec4dc08b3829-0_1776821307748.png" alt="Convex logo" width="28" height="28"> Convex: Universal API

Connect Convex's Management API to read team and project metadata using bearer-token authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/convex/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://convex.dev
- **Vendor API docs:** https://docs.convex.dev/management-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Details](actions/get-token-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Deployments

| Action | Method | Description |
| --- | --- | --- |
| [Create Deployment](actions/create-deployment.md) | POST | Creates a new deployment in Convex. |
| [Delete Deployment](actions/delete-deployment.md) | DELETE | Deletes an existing deployment from Convex. |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves a Convex deployment by name. |
| [Get Project Deployment](actions/get-project-deployment.md) | GET | Retrieves a deployment from a Convex project. |
| [Get Project Deployment By Slug](actions/get-project-deployment-by-slug.md) | GET | Retrieves a deployment from Convex by project slug. |
| [List Deployment Classes](actions/list-deployment-classes.md) | GET | Retrieves deployment classes from a Convex team. |
| [List Deployment Regions](actions/list-deployment-regions.md) | GET | Retrieves deployment regions from a Convex team. |
| [List Local Deployments](actions/list-local-deployments.md) | GET | Retrieves local deployments from a Convex team. |
| [List Project Deployments](actions/list-project-deployments.md) | GET | Retrieves deployments from a Convex project. |
| [List Team Deployments](actions/list-team-deployments.md) | GET | Retrieves deployments from a Convex team. |
| [Update Deployment](actions/update-deployment.md) | PUT | Updates an existing deployment in Convex. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [List Default Environment Variables](actions/list-default-environment-variables.md) | GET | Retrieves default environment variables from a Convex project. |
| [Update Default Environment Variables](actions/update-default-environment-variables.md) | PUT | Updates default environment variables in Convex. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Convex. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Convex. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Convex by ID. |
| [Get Project By Slug](actions/get-project-by-slug.md) | GET | Retrieves a project from Convex by slug. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Convex team. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [List Preview Deploy Keys](actions/list-preview-deploy-keys.md) | GET | Retrieves preview deploy keys from a Convex project. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Details](actions/get-token-details.md) | GET | Retrieves details about the current Convex token. |

