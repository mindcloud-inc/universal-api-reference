# Mendix: Native API Reference

A consolidated summary of Mendix's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.mendix.com/apidocs-mxsdk/apidocs/
- **OpenAPI specification:** https://raw.githubusercontent.com/mendix/docs/development/static/openapi-spec/projects-v2.yaml
- **REST API base URL:** `https://projects-api.home.mendix.com/v2`
- **REST API base URL:** `https://projects-api.home.mendix.com/v2`

## Authentication

### Personal Access Token

Use a Mendix Personal Access Token (PAT). Mendix platform APIs expect this credential in the Authorization header as `MxToken <PAT>`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.mendix.com/portal/user-settings/#personal-access-tokens)

## API conventions

### REST API

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

### REST API

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

- **REST API:** Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.
- **REST API:** Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

- **REST API:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
- **REST API:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project Member](actions/add-project-member.md) | `POST /projects/:projectId/members` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:projectId` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Get Project Creation Job](actions/get-project-creation-job.md) | `GET /projects/jobs/:jobId` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Get Project Role](actions/get-project-role.md) | `GET /roles/:roleId` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [List Account Project Roles](actions/list-account-project-roles.md) | `GET /accounts/:accountId/roles` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [List Account Projects](actions/list-account-projects.md) | `GET /accounts/:accountId/projects` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [List Project Members](actions/list-project-members.md) | `GET /projects/:projectId/members` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [List User Projects](actions/list-user-projects.md) | `GET /users/:userId/projects` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Remove Project Member](actions/remove-project-member.md) | `DELETE /projects/:projectId/members/:userId` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Update Project Categories](actions/update-project-categories.md) | `PATCH /projects/:projectId` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
| [Update Project Member](actions/update-project-member.md) | `PATCH /projects/:projectId/members/:userId` | [docs](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/) |
