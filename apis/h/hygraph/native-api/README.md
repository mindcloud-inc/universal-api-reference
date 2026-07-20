# Hygraph: Native API Reference

A consolidated summary of Hygraph's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://hygraph.com/docs/api-reference
- **API base URL:** `{endpoint}`

## Authentication

### Permanent Auth Token

Use a Hygraph Permanent Auth Token for the project/environment endpoint you want this connection to access.

### Credentials

- **API Key:** `apiKey` · required
- **Content API Endpoint:** `endpoint` · required · The full Hygraph Content API endpoint for one project environment, for example https://api-eu-central-1.hygraph.com/v2/projectId/master.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hygraph.com/docs/api-reference/basics/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Asset From Remote URL](actions/create-asset-from-remote-url.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/assets/uploading-assets) |
| [Delete Asset](actions/delete-asset.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/assets/deleting-assets) |
| [Execute GraphQL Mutation](actions/execute-graphql-mutation.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/content-api/mutations) |
| [Execute GraphQL Query](actions/execute-graphql-query.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/content-api/queries) |
| [Get Asset](actions/get-asset.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/assets/fetching-assets) |
| [Introspect Schema](actions/introspect-schema.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/content-api/queries) |
| [List Assets](actions/list-assets.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/assets/fetching-assets) |
| [Publish Asset](actions/publish-asset.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/assets/publishing-assets) |
| [Unpublish Asset](actions/unpublish-asset.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/assets/publishing-assets) |
| [Update Asset Remote URL](actions/update-asset-remote-url.md) | `POST` | [docs](https://hygraph.com/docs/api-reference/assets/updating-assets) |
