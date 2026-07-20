# Sourcegraph: Native API Reference

A consolidated summary of Sourcegraph's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://sourcegraph.com/docs/api
- **API base URL:** `https://sourcegraph.com`

## Authentication

### Access Token

Use a Sourcegraph access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sourcegraph.com/docs/cli/how-tos/creating-an-access-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Saved Search](actions/create-saved-search.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Create Search Context](actions/create-search-context.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Delete Saved Search](actions/delete-saved-search.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Delete Search Context](actions/delete-search-context.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Client Configuration](actions/get-client-configuration.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Current User](actions/get-current-user.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Namespace By Name](actions/get-namespace-by-name.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Organization By Name](actions/get-organization-by-name.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Repository By Name](actions/get-repository-by-name.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Search Context By Spec](actions/get-search-context-by-spec.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Site Info](actions/get-site-info.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get User By Username](actions/get-user-by-username.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Get Viewer Settings](actions/get-viewer-settings.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [List Repositories](actions/list-repositories.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [List Saved Searches](actions/list-saved-searches.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [List Search Contexts](actions/list-search-contexts.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Parse Search Query](actions/parse-search-query.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Run Search](actions/run-search.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Update Saved Search](actions/update-saved-search.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
| [Update Search Context](actions/update-search-context.md) | `POST /.api/graphql` | [docs](https://sourcegraph.com/docs/api/graphql) |
