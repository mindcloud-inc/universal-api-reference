# WebCategorize: Native API Reference

A consolidated summary of WebCategorize's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://webcategorize.com/api/
- **OpenAPI specification:** https://webcategorize.com/webcategorize.json
- **API base URL:** `https://app.webcategorize.com/api`

## Authentication

### API Key

Connect WebCategorize using an API key from the WebCategorize API Keys page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://webcategorize.com/webcategorize.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Content Feedback](actions/add-content-feedback.md) | `POST /html/feedback/{contentId}` | [docs](https://webcategorize.com/webcategorize.json) |
| [Add URL Feedback](actions/add-url-feedback.md) | `POST /url/feedback/{urlId}` | [docs](https://webcategorize.com/webcategorize.json) |
| [Categorize Content](actions/categorize-content.md) | `POST /html` | [docs](https://webcategorize.com/webcategorize.json) |
| [Categorize URL](actions/categorize-url.md) | `POST /url` | [docs](https://webcategorize.com/webcategorize.json) |
| [Create API Key](actions/create-api-key.md) | `POST /keys` | [docs](https://webcategorize.com/webcategorize.json) |
| [List API Keys](actions/list-api-keys.md) | `GET /keys` | [docs](https://webcategorize.com/webcategorize.json) |
| [List Content Categorizations](actions/list-content-categorizations.md) | `GET /html/get/all` | [docs](https://webcategorize.com/webcategorize.json) |
| [List Content Tags](actions/list-content-tags.md) | `GET /html/get/tags` | [docs](https://webcategorize.com/webcategorize.json) |
| [List URL Categorizations](actions/list-url-categorizations.md) | `GET /url/get/all` | [docs](https://webcategorize.com/webcategorize.json) |
| [List URL Tags](actions/list-url-tags.md) | `GET /url/get/tags` | [docs](https://webcategorize.com/webcategorize.json) |
| [Retrieve Content Categorization](actions/retrieve-content-categorization.md) | `GET /html/{contentId}` | [docs](https://webcategorize.com/webcategorize.json) |
| [Retrieve URL Categorization](actions/retrieve-url-categorization.md) | `GET /url/{urlId}` | [docs](https://webcategorize.com/webcategorize.json) |
