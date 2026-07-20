# MantisBT: Native API Reference

A consolidated summary of MantisBT's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://github.com/mantisbt/mantisbt/blob/master/api/rest/mantisbt_openapi.yaml
- **OpenAPI specification:** https://raw.githubusercontent.com/mantisbt/mantisbt/master/api/rest/mantisbt_openapi.yaml
- **API base URL:** `{baseUrl}/api/rest`

## Authentication

### API Token

Use a MantisBT API token passed as the raw value of the Authorization header.

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · Root URL of your MantisBT or MantisHub instance, with no trailing slash. Example: https://mindcloud-stage0.mantishub.io

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | `POST /issues` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Create Issue Note](actions/create-issue-note.md) | `POST /issues/{issue_id}/notes` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Create Project Version](actions/create-project-version.md) | `POST /projects/{project_id}/versions` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Delete Issue Note](actions/delete-issue-note.md) | `DELETE /issues/{issue_id}/notes/{issue_note_id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Delete Project Version](actions/delete-project-version.md) | `DELETE /projects/{project_id}/versions/{version_id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Configuration Options](actions/get-configuration-options.md) | `GET /config` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Issue](actions/get-issue.md) | `GET /issues/{issue_id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Issues](actions/get-issues.md) | `GET /issues` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Localized Strings](actions/get-localized-strings.md) | `GET /lang` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get My User Info](actions/get-my-user-info.md) | `GET /users/me` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Project](actions/get-project.md) | `GET /projects/{project_id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Project Handlers](actions/get-project-handlers.md) | `GET /projects/{project_id}/handlers` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Project Users](actions/get-project-users.md) | `GET /projects/{project_id}/users` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Project Version](actions/get-project-version.md) | `GET /projects/{project_id}/versions/{version_id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Project Versions](actions/get-project-versions.md) | `GET /projects/{project_id}/versions` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get Projects](actions/get-projects.md) | `GET /projects` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get User](actions/get-user.md) | `GET /users/{id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Get User By Username](actions/get-user-by-username.md) | `GET /users/username/{username}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Monitor Issue](actions/monitor-issue.md) | `POST /issues/{issue_id}/monitors` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Update Issue](actions/update-issue.md) | `PATCH /issues/{issue_id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
| [Update Project Version](actions/update-project-version.md) | `PATCH /projects/{project_id}/versions/{version_id}` | [docs](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml) |
