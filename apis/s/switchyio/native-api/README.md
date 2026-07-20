# Switchy.io: Native API Reference

A consolidated summary of Switchy.io's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developers.switchy.io/docs/overview/index
- **API base URL:** `https://graphql.switchy.io`

## Authentication

### API Token Header

Use the Switchy workspace token via the Api-Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Api-Authorization: <apiKey>
```

[Official authentication documentation](https://developers.switchy.io/docs/overview/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the request body to set the page size (default 2; accepted range 1–100). Use `offset` in the request body as the record offset; numbering starts at 0.

## Filtering

Send filters in the request body. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `order_by` in the request body. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Delete Links](actions/bulk-delete-links.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/overview/root-endpoint) |
| [Bulk Update Links](actions/bulk-update-links.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/overview/root-endpoint) |
| [Count Workspaces](actions/count-workspaces.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Create Link](actions/create-link.md) | `POST https://api.switchy.io/v1/links/create` | [docs](https://developers.switchy.io/docs/guides/how-to-create-a-link) |
| [Delete Link](actions/delete-link.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/overview/root-endpoint) |
| [Get Domain](actions/get-domain.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Get Folder](actions/get-folder.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Get Link](actions/get-link.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Get Link Script](actions/get-link-script.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Get Pixel](actions/get-pixel.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Get Token](actions/get-token.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Get UTM Template](actions/get-utm-template.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Get Workspace](actions/get-workspace.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List Domains](actions/list-domains.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List Folders](actions/list-folders.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List Link Scripts](actions/list-link-scripts.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List Links](actions/list-links.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List Pixels](actions/list-pixels.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List Tokens](actions/list-tokens.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List UTM Templates](actions/list-utm-templates.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [List Workspaces](actions/list-workspaces.md) | `POST /v1/graphql` | [docs](https://developers.switchy.io/docs/guides/how-to-query) |
| [Update Link](actions/update-link.md) | `PUT https://api.switchy.io/v1/links/by-domain/:domain/:id` | [docs](https://developers.switchy.io/docs/guides/how-to-update-a-link) |
