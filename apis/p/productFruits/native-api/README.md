# Product Fruits: Native API Reference

A consolidated summary of Product Fruits's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://help.productfruits.com/en/article/rest-api-authentication
- **API base URL:** `https://api.productfruits.com`

## Authentication

### API Key

Authenticate Product Fruits requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.productfruits.com/en/article/rest-api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `categories`.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | `POST /v1/feedback` | [docs](https://help.productfruits.com/en/article/server-api-feedback) |
| [Delete Article Content by Language](actions/delete-article-content-by-language.md) | `DELETE /v1/knowledgebase/articles/:correlationId/content/:lang` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-delete-article--by-language-endpoint) |
| [Delete Article Content Version](actions/delete-article-content-version.md) | `DELETE /v1/knowledgebase/articles/:correlationId/content/:lang/:id` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-delete-article-content-version-endpoint) |
| [Delete Knowledge Base Article](actions/delete-knowledge-base-article.md) | `DELETE /v1/knowledgebase/articles/:correlationId` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-delete-article-endpoint) |
| [Delete Knowledge Base Category](actions/delete-knowledge-base-category.md) | `DELETE /v1/knowledgebase/categories/:correlationId` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-delete-category) |
| [Delete User](actions/delete-user.md) | `DELETE /v1/users/:username` | [docs](https://help.productfruits.com/en/article/restp-api-users-management) |
| [Get Knowledge Base Category](actions/get-knowledge-base-category.md) | `GET /v1/knowledgebase/categories/:correlationId` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-get-specific-category) |
| [Identify User](actions/identify-user.md) | `POST /v1/identify` | [docs](https://help.productfruits.com/en/article/rest-api-user-identification) |
| [Import Knowledge Base Articles](actions/import-knowledge-base-articles.md) | `POST /v1/knowledgebase/import` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-import-articles-endpoint) |
| [Import Knowledge Base Categories](actions/import-knowledge-base-categories.md) | `POST /v1/knowledgebase/categories/import` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-import-categories) |
| [List Knowledge Base Articles](actions/list-knowledge-base-articles.md) | `GET /v1/knowledgebase/articles` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-list-articles-endpoint) |
| [List Knowledge Base Categories](actions/list-knowledge-base-categories.md) | `GET /v1/knowledgebase/categories` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-list-categories) |
| [Track Event](actions/track-event.md) | `POST /v1/events/track` | [docs](https://help.productfruits.com/en/article/events-tracking) |
| [Update Knowledge Base Category](actions/update-knowledge-base-category.md) | `PUT /v1/knowledgebase/categories/:correlationId` | [docs](https://help.productfruits.com/en/article/knowledge-base-api-update-specific-category) |
