# Cloudsmith: Native API Reference

A consolidated summary of Cloudsmith's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://help.cloudsmith.io/reference/
- **API base URL:** `https://api.cloudsmith.io`

## Authentication

### API Key

Authenticate with a Cloudsmith API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://help.cloudsmith.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page_size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Basic API Connectivity](actions/check-basic-api-connectivity.md) | `GET /status/check/basic/` | [docs](https://help.cloudsmith.io/reference/status_check_basic) |
| [Create Organization Team](actions/create-organization-team.md) | `POST /orgs/:org/teams/` | [docs](https://help.cloudsmith.io/reference/orgs_teams_create) |
| [Create Repository](actions/create-repository.md) | `POST /repos/:owner/` | [docs](https://help.cloudsmith.io/reference/repos_create) |
| [Delete Organization Team](actions/delete-organization-team.md) | `DELETE /orgs/:org/teams/:team/` | [docs](https://help.cloudsmith.io/reference/orgs_teams_delete) |
| [Delete Repository](actions/delete-repository.md) | `DELETE /repos/:owner/:identifier/` | [docs](https://help.cloudsmith.io/reference/repos_delete) |
| [Get Current Rate Limits](actions/get-current-rate-limits.md) | `GET /rates/limits/` | [docs](https://help.cloudsmith.io/reference/rates_limits_list) |
| [Get Current User](actions/get-current-user.md) | `GET /user/self/` | [docs](https://help.cloudsmith.io/reference/user_self) |
| [Get Distro](actions/get-distro.md) | `GET /distros/:slug/` | [docs](https://help.cloudsmith.io/reference/distros_read) |
| [Get Format](actions/get-format.md) | `GET /formats/:slug/` | [docs](https://help.cloudsmith.io/reference/formats_read) |
| [Get Namespace](actions/get-namespace.md) | `GET /namespaces/:slug/` | [docs](https://help.cloudsmith.io/reference/namespaces_read) |
| [Get Organization](actions/get-organization.md) | `GET /orgs/:org/` | [docs](https://help.cloudsmith.io/reference/orgs_read) |
| [Get Organization Team](actions/get-organization-team.md) | `GET /orgs/:org/teams/:team/` | [docs](https://help.cloudsmith.io/reference/orgs_teams_read) |
| [Get Repository](actions/get-repository.md) | `GET /repos/:owner/:identifier/` | [docs](https://help.cloudsmith.io/reference/repos_read) |
| [List Distros](actions/list-distros.md) | `GET /distros/` | [docs](https://help.cloudsmith.io/reference/distros_list) |
| [List Formats](actions/list-formats.md) | `GET /formats/` | [docs](https://help.cloudsmith.io/reference/formats_list) |
| [List Namespaces](actions/list-namespaces.md) | `GET /namespaces/` | [docs](https://help.cloudsmith.io/reference/namespaces_list) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs/` | [docs](https://help.cloudsmith.io/reference/orgs_list) |
| [List Repositories for Current User](actions/list-repositories-for-current-user.md) | `GET /repos/` | [docs](https://help.cloudsmith.io/reference/repos_user_list) |
| [Update Organization Team](actions/update-organization-team.md) | `PATCH /orgs/:org/teams/:team/` | [docs](https://help.cloudsmith.io/reference/orgs_teams_partial_update) |
| [Update Repository](actions/update-repository.md) | `PATCH /repos/:owner/:identifier/` | [docs](https://help.cloudsmith.io/reference/repos_partial_update) |
