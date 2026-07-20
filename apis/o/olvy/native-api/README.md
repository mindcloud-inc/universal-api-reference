# Olvy: Native API Reference

A consolidated summary of Olvy's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://app.olvy.co/settings/api
- **API base URL:** `https://app.olvy.co/api/v2/graphql`

## Authentication

### API Key

Use an Olvy API key together with the workspace alias/subdomain for workspace-scoped GraphQL access.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace Alias:** `workspaceAlias` · required · Use the Olvy workspace alias/subdomain, such as `mindcloud`, so actions can resolve the workspace-scoped organisation.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.olvy.co/mindcloud/settings/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | `POST /` | [docs](https://app.olvy.co/settings/api) |
| [Get Organisation](actions/get-organisation.md) | `POST /` | [docs](https://app.olvy.co/settings/api) |
| [Get Project](actions/get-project.md) | `POST /` | [docs](https://app.olvy.co/settings/api) |
| [List Categories](actions/list-categories.md) | `POST /` | [docs](https://app.olvy.co/settings/api) |
| [List Projects](actions/list-projects.md) | `POST /` | [docs](https://app.olvy.co/settings/api) |
| [Query](actions/query.md) | `POST /` | [docs](https://app.olvy.co/settings/api) |
| [Validate Email](actions/validate-email.md) | `POST /` | [docs](https://app.olvy.co/settings/api) |
