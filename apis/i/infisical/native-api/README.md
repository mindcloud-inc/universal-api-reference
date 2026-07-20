# Infisical: Native API Reference

A consolidated summary of Infisical's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://infisical.com/docs/api-reference/overview/introduction
- **API base URL:** `https://app.infisical.com`

## Authentication

### Universal Auth

Authenticate with Infisical Universal Auth using machine identity credentials.

### Credentials

- **Client ID:** `clientId` · required · Your Infisical machine identity Client ID.
- **Client Secret:** `clientSecret` · required · Your Infisical machine identity Client Secret.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://infisical.com/docs/documentation/platform/identities/universal-auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /api/v1/auth/universal-auth/login` | [docs](https://infisical.com/docs/api-reference/endpoints/universal-auth/login) |
| [Create Environment](actions/create-environment.md) | `POST /api/v1/projects/:projectId/environments` | [docs](https://infisical.com/docs/api-reference/endpoints/environments/create) |
| [Create Folder](actions/create-folder.md) | `POST /api/v2/folders` | [docs](https://infisical.com/docs/api-reference/endpoints/folders/create) |
| [Create Project](actions/create-project.md) | `POST /api/v1/projects` | [docs](https://infisical.com/docs/api-reference/endpoints/projects/create-project) |
| [Create Secret](actions/create-secret.md) | `POST /api/v4/secrets/:secretName` | [docs](https://infisical.com/docs/api-reference/endpoints/secrets/create) |
| [Create Tag](actions/create-tag.md) | `POST /api/v1/projects/:projectId/tags` | [docs](https://infisical.com/docs/api-reference/endpoints/secret-tags/create) |
| [Delete Environment](actions/delete-environment.md) | `DELETE /api/v1/projects/:projectId/environments/:id` | [docs](https://infisical.com/docs/api-reference/endpoints/environments/delete) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /api/v2/folders/:folderIdOrName` | [docs](https://infisical.com/docs/api-reference/endpoints/folders/delete) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v1/projects/:projectId` | [docs](https://infisical.com/docs/api-reference/endpoints/projects/delete-project) |
| [Delete Secret](actions/delete-secret.md) | `DELETE /api/v4/secrets/:secretName` | [docs](https://infisical.com/docs/api-reference/endpoints/secrets/delete) |
| [Get Folder By ID](actions/get-folder-by-id.md) | `GET /api/v2/folders/:id` | [docs](https://infisical.com/docs/api-reference/endpoints/folders/get-by-id) |
| [Get Project](actions/get-project.md) | `GET /api/v1/projects/:projectId` | [docs](https://infisical.com/docs/api-reference/endpoints/projects/get-project) |
| [Get Project By Slug](actions/get-project-by-slug.md) | `GET /api/v1/projects/slug/:slug` | [docs](https://infisical.com/docs/api-reference/endpoints/projects/get-project-by-slug) |
| [List Folders](actions/list-folders.md) | `GET /api/v2/folders` | [docs](https://infisical.com/docs/api-reference/endpoints/folders/list) |
| [List Projects](actions/list-projects.md) | `GET /api/v1/projects` | [docs](https://infisical.com/docs/api-reference/endpoints/projects/list-projects) |
| [List Secrets](actions/list-secrets.md) | `GET /api/v4/secrets` | [docs](https://infisical.com/docs/api-reference/endpoints/secrets/list) |
| [List Tags](actions/list-tags.md) | `GET /api/v1/projects/:projectId/tags` | [docs](https://infisical.com/docs/api-reference/endpoints/secret-tags/list) |
| [Retrieve Secret](actions/retrieve-secret.md) | `GET /api/v4/secrets/:secretName` | [docs](https://infisical.com/docs/api-reference/endpoints/secrets/read) |
| [Update Environment](actions/update-environment.md) | `PATCH /api/v1/projects/:projectId/environments/:id` | [docs](https://infisical.com/docs/api-reference/endpoints/environments/update) |
| [Update Project](actions/update-project.md) | `PATCH /api/v1/projects/:projectId` | [docs](https://infisical.com/docs/api-reference/endpoints/projects/update-project) |
| [Update Secret](actions/update-secret.md) | `PATCH /api/v4/secrets/:secretName` | [docs](https://infisical.com/docs/api-reference/endpoints/secrets/update) |
