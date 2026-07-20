# Vercel: Native API Reference

A consolidated summary of Vercel's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://vercel.com/docs/rest-api
- **API base URL:** `https://api.vercel.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://vercel.com/docs/rest-api#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `from` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | `POST /v7/domains` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains/add-an-existing-domain-to-the-vercel-platform) |
| [Add Project Domain](actions/add-project-domain.md) | `POST /v10/projects/:idOrName/domains` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/add-a-domain-to-a-project) |
| [Assign Alias](actions/assign-alias.md) | `POST /v2/deployments/:id/aliases` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/aliases/assign-an-alias) |
| [Cancel Deployment](actions/cancel-deployment.md) | `PATCH /v12/deployments/:id/cancel` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/cancel-a-deployment) |
| [Create Deployment](actions/create-deployment.md) | `POST /v13/deployments` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/create-a-new-deployment) |
| [Create DNS Record](actions/create-dns-record.md) | `POST /v2/domains/:domain/records` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns/create-a-dns-record) |
| [Create Project](actions/create-project.md) | `POST /v11/projects` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/create-a-new-project) |
| [Create Project Env Vars](actions/create-project-env-vars.md) | `POST /v10/projects/:idOrName/env` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/create-one-or-more-environment-variables) |
| [Delete Alias](actions/delete-alias.md) | `DELETE /v2/aliases/:aliasId` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/aliases/delete-an-alias) |
| [Delete Deployment](actions/delete-deployment.md) | `DELETE /v13/deployments/:id` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/delete-a-deployment) |
| [Delete DNS Record](actions/delete-dns-record.md) | `DELETE /v2/domains/:domain/records/:recordId` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns/delete-a-dns-record) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /v6/domains/:domain` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains/remove-a-domain-by-name) |
| [Delete Project](actions/delete-project.md) | `DELETE /v9/projects/:idOrName` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/delete-a-project) |
| [Delete Project Env Var](actions/delete-project-env-var.md) | `DELETE /v9/projects/:idOrName/env/:id` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/remove-an-environment-variable) |
| [Get Alias](actions/get-alias.md) | `GET /v4/aliases/:idOrAlias` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/aliases/get-an-alias) |
| [Get Deployment](actions/get-deployment.md) | `GET /v13/deployments/:idOrUrl` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/get-a-deployment-by-id-or-url) |
| [Get Deployment Events](actions/get-deployment-events.md) | `GET /v3/deployments/:idOrUrl/events` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments) |
| [Get Domain](actions/get-domain.md) | `GET /v5/domains/:domain` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains/get-information-for-a-single-domain) |
| [Get Domain Config](actions/get-domain-config.md) | `GET /v6/domains/:domain/config` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains) |
| [Get Project](actions/get-project.md) | `GET /v9/projects/:idOrName` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/find-a-project-by-id-or-name) |
| [Get Project Domain](actions/get-project-domain.md) | `GET /v9/projects/:idOrName/domains/:domain` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/get-a-project-domain) |
| [Get Project Env Var](actions/get-project-env-var.md) | `GET /v1/projects/:idOrName/env/:id` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-the-decrypted-value-of-an-environment-variable-of-a-project-by-id) |
| [Get User](actions/get-user.md) | `GET /v2/user` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/user/get-the-user) |
| [List Aliases](actions/list-aliases.md) | `GET /v4/aliases` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/aliases/list-aliases) |
| [List Deployment Files](actions/list-deployment-files.md) | `GET /v6/deployments/:id/files` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/list-deployment-files) |
| [List Deployments](actions/list-deployments.md) | `GET /v6/deployments` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/list-deployments) |
| [List DNS Records](actions/list-dns-records.md) | `GET /v4/domains/:domain/records` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns) |
| [List Domains](actions/list-domains.md) | `GET /v5/domains` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains/list-all-the-domains) |
| [List Project Domains](actions/list-project-domains.md) | `GET /v9/projects/:idOrName/domains` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-project-domains-by-project-by-id-or-name) |
| [List Project Env Vars](actions/list-project-env-vars.md) | `GET /v10/projects/:idOrName/env` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-the-environment-variables-of-a-project-by-id-or-name) |
| [List Projects](actions/list-projects.md) | `GET /v10/projects` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-a-list-of-projects) |
| [List Teams](actions/list-teams.md) | `GET /v2/teams` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/teams/list-all-teams) |
| [Pause Project](actions/pause-project.md) | `POST /v1/projects/:projectId/pause` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/pause-a-project) |
| [Remove Project Domain](actions/remove-project-domain.md) | `DELETE /v9/projects/:idOrName/domains/:domain` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/remove-a-domain-from-a-project) |
| [Unpause Project](actions/unpause-project.md) | `POST /v1/projects/:projectId/unpause` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/unpause-a-project) |
| [Update DNS Record](actions/update-dns-record.md) | `PATCH /v1/domains/records/:recordId` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns/update-an-existing-dns-record) |
| [Update Project](actions/update-project.md) | `PATCH /v9/projects/:idOrName` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/update-an-existing-project) |
| [Update Project Domain](actions/update-project-domain.md) | `PATCH /v9/projects/:idOrName/domains/:domain` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/update-a-project-domain) |
| [Update Project Env Var](actions/update-project-env-var.md) | `PATCH /v9/projects/:idOrName/env/:id` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/edit-an-environment-variable) |
| [Verify Project Domain](actions/verify-project-domain.md) | `POST /v9/projects/:idOrName/domains/:domain/verify` | [docs](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/verify-project-domain) |
