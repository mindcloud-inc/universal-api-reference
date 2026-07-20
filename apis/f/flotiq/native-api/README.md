# Flotiq: Native API Reference

A consolidated summary of Flotiq's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://flotiq.com/docs/API/
- **OpenAPI specification:** https://api.flotiq.com/api/v1/open-api-schema.json
- **API base URL:** `https://api.flotiq.com/api/v1`

## Authentication

### API Key

Use a Flotiq Application or User Defined API key.

### Credentials

- **API key:** `apiKey` · required

Send these headers with each API request:

```http
X-AUTH-TOKEN: <apiKey>
```

[Official authentication documentation](https://flotiq.com/docs/API/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `total_pages`. The current page number is read from `current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `lt`.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Content Object](actions/archive-content-object.md) | `POST /content/{{name}}/{{id}}/archive` | [docs](https://flotiq.com/docs/API/draft-public/) |
| [Batch Archive Content Objects](actions/batch-archive-content-objects.md) | `POST /content/{{name}}/batch-archive` | [docs](https://flotiq.com/docs/API/draft-public/) |
| [Batch Create Content Objects](actions/batch-create-content-objects.md) | `POST /content/{{name}}/batch` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Batch Delete Content Objects](actions/batch-delete-content-objects.md) | `POST /content/{{name}}/batch-delete` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Batch Delete Media Objects](actions/batch-delete-media-objects.md) | `POST /content/_media/batch-delete` | [docs](https://flotiq.com/docs/API/media/) |
| [Batch Patch Content Objects](actions/batch-patch-content-objects.md) | `PATCH /content/{{name}}/batch` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Batch Patch Media Objects](actions/batch-patch-media-objects.md) | `PATCH /content/_media/batch` | [docs](https://flotiq.com/docs/API/media/) |
| [Batch Publish Content Objects](actions/batch-publish-content-objects.md) | `POST /content/{{name}}/batch-publish` | [docs](https://flotiq.com/docs/API/draft-public/) |
| [Batch Unpublish Content Objects](actions/batch-unpublish-content-objects.md) | `POST /content/{{name}}/batch-unpublish` | [docs](https://flotiq.com/docs/API/draft-public/) |
| [Create Content Object](actions/create-content-object.md) | `POST /content/{{name}}` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Create Content Type](actions/create-content-type.md) | `POST /internal/contenttype` | [docs](https://flotiq.com/docs/API/content-types/) |
| [Delete Content Object](actions/delete-content-object.md) | `DELETE /content/{{name}}/{{id}}` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Delete Content Type](actions/delete-content-type.md) | `DELETE /internal/contenttype/{{id}}` | [docs](https://flotiq.com/docs/API/content-types/) |
| [Delete Media Object](actions/delete-media-object.md) | `DELETE /content/_media/{{id}}` | [docs](https://flotiq.com/docs/API/media/) |
| [Get Auth Context](actions/get-auth-context.md) | `GET https://api.flotiq.com/api/auth-context` | [docs](https://flotiq.com/docs/API/get-started/) |
| [Get Content Object](actions/get-content-object.md) | `GET /content/{{name}}/{{id}}` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Get Content Type](actions/get-content-type.md) | `GET /internal/contenttype/{{id}}` | [docs](https://flotiq.com/docs/API/content-types/) |
| [Get GraphQL Schema](actions/get-graphql-schema.md) | `GET https://api.flotiq.com/api/v2/graphql/schema` | [docs](https://flotiq.com/docs/API/graph-ql/) |
| [Get Media Image](actions/get-media-image.md) | `GET https://api.flotiq.com/image/{{widthHeight}}/{{key}}` | [docs](https://flotiq.com/docs/API/media/) |
| [Get Media Object](actions/get-media-object.md) | `GET /content/_media/{{id}}` | [docs](https://flotiq.com/docs/API/media/) |
| [Get Media Version](actions/get-media-version.md) | `GET /content/_media/{{id}}/version/{{versionId}}` | [docs](https://flotiq.com/docs/API/media/) |
| [Get OpenAPI Schema](actions/get-openapi-schema.md) | `GET /open-api-schema.json` | [docs](https://flotiq.com/docs/API/open-api-schema/) |
| [List Content Objects](actions/list-content-objects.md) | `GET /content/{{name}}` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [List Content Types](actions/list-content-types.md) | `GET /internal/contenttype` | [docs](https://flotiq.com/docs/API/content-type/listing-ctd/) |
| [List Media Objects](actions/list-media-objects.md) | `GET /content/_media` | [docs](https://flotiq.com/docs/API/media/) |
| [List Media Versions](actions/list-media-versions.md) | `GET /content/_media/{{id}}/version` | [docs](https://flotiq.com/docs/API/media/) |
| [List Removed Content Objects](actions/list-removed-content-objects.md) | `GET /content/{{name}}/removed` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [List Removed Media Objects](actions/list-removed-media-objects.md) | `GET /content/_media/removed` | [docs](https://flotiq.com/docs/API/media/) |
| [Patch Content Object](actions/patch-content-object.md) | `PATCH /content/{{name}}/{{id}}` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Patch Media Object](actions/patch-media-object.md) | `PATCH /content/_media/{{id}}` | [docs](https://flotiq.com/docs/API/media/) |
| [Publish Content Object](actions/publish-content-object.md) | `POST /content/{{name}}/{{id}}/publish` | [docs](https://flotiq.com/docs/API/draft-public/) |
| [Run GraphQL Query](actions/run-graphql-query.md) | `POST https://api.flotiq.com/api/v2/graphql` | [docs](https://flotiq.com/docs/API/graph-ql/) |
| [Search Content](actions/search-content.md) | `GET /search` | [docs](https://flotiq.com/docs/API/search/) |
| [Unpublish Content Object](actions/unpublish-content-object.md) | `POST /content/{{name}}/{{id}}/unpublish` | [docs](https://flotiq.com/docs/API/draft-public/) |
| [Update Content Object](actions/update-content-object.md) | `PUT /content/{{name}}/{{id}}` | [docs](https://flotiq.com/docs/API/content-objects/) |
| [Update Content Type](actions/update-content-type.md) | `PUT /internal/contenttype/{{id}}` | [docs](https://flotiq.com/docs/API/content-types/) |
| [Update Media Object](actions/update-media-object.md) | `PUT /content/_media/{{id}}` | [docs](https://flotiq.com/docs/API/media/) |
| [Upload Media](actions/upload-media.md) | `POST https://api.flotiq.com/api/media` | [docs](https://flotiq.com/docs/API/media-library/) |
