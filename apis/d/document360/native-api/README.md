# Document360: Native API Reference

A consolidated summary of Document360's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.document360.com/apidocs/introduction
- **OpenAPI specification:** https://apihub.document360.io/swagger/v2/swagger.json
- **API base URL:** `https://apihub.document360.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.document360.com/apidocs/generating-api-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | `POST /v2/Articles` | [docs](https://apidocs.document360.com/apidocs/add-an-article) |
| [Create Category](actions/create-category.md) | `POST /v2/Categories` | [docs](https://apidocs.document360.com/apidocs/add-a-category) |
| [Fork Article](actions/fork-article.md) | `PUT /v2/Articles/:articleId/fork` | [docs](https://apidocs.document360.com/apidocs/fork-an-article) |
| [Fork Category Page](actions/fork-category-page.md) | `PUT /v2/Categories/:categoryId/fork` | [docs](https://apidocs.document360.com/apidocs/fork-category-page-with-an-id) |
| [Get Article](actions/get-article.md) | `GET /v2/Articles/:articleId/:langCode` | [docs](https://apidocs.document360.com/apidocs/get-article) |
| [Get Article by URL](actions/get-article-by-url.md) | `GET /v2/Articles` | [docs](https://apidocs.document360.com/apidocs/gets-an-article-by-url) |
| [Get Article by Version](actions/get-article-by-version.md) | `GET /v2/Articles/:articleId/:langCode/versions/:versionNumber` | [docs](https://apidocs.document360.com/apidocs/get-article-by-version) |
| [Get Category](actions/get-category.md) | `GET /v2/Categories/:categoryId` | [docs](https://apidocs.document360.com/apidocs/get-category) |
| [Get Category Page](actions/get-category-page.md) | `GET /v2/Categories/:categoryId/content/:langCode` | [docs](https://apidocs.document360.com/apidocs/get-category-page-with-an-id) |
| [Get Document by URL Path](actions/get-document-by-url-path.md) | `GET /v2/Project/Document` | [docs](https://apidocs.document360.com/apidocs/get-a-document-article-or-category-by-url-path) |
| [List Article Versions](actions/list-article-versions.md) | `GET /v2/Articles/:articleId/:langCode/versions` | [docs](https://apidocs.document360.com/apidocs/get-article-versions) |
| [List Articles in Project Version](actions/list-articles-in-project-version.md) | `GET /v2/ProjectVersions/:projectVersionId/articles` | [docs](https://apidocs.document360.com/apidocs/project-version-articles) |
| [List Categories in Project Version](actions/list-categories-in-project-version.md) | `GET /v2/ProjectVersions/:projectVersionId/categories` | [docs](https://apidocs.document360.com/apidocs/project-version-categories) |
| [List Project Versions](actions/list-project-versions.md) | `GET /v2/ProjectVersions` | [docs](https://apidocs.document360.com/apidocs/get-project-versions) |
| [List Version Languages](actions/list-version-languages.md) | `GET /v2/Language/:projectVersionId` | [docs](https://apidocs.document360.com/apidocs/gets-all-version-languages-in-the-project) |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | `GET /v2/Project/workflow-statuses` | [docs](https://apidocs.document360.com/apidocs/gets-all-workflow-statuses-for-a-project) |
| [Publish Article](actions/publish-article.md) | `POST /v2/Articles/:articleId/:langCode/publish` | [docs](https://apidocs.document360.com/apidocs/publish-an-article) |
| [Publish Category](actions/publish-category.md) | `POST /v2/Categories/:categoryId/:langCode/publish` | [docs](https://apidocs.document360.com/apidocs/publishes-an-category-with-an-id) |
| [Search Articles by Translation Status](actions/search-articles-by-translation-status.md) | `GET /v2/Translations/:projectVersionId/:langCode` | [docs](https://apidocs.document360.com/apidocs/gets-article-to-be-translated) |
| [Search Articles in Project Version](actions/search-articles-in-project-version.md) | `GET /v2/ProjectVersions/:projectVersionId/:langCode` | [docs](https://apidocs.document360.com/apidocs/search-inside-project-version) |
| [Update Article](actions/update-article.md) | `PUT /v2/Articles/:articleId/:langCode` | [docs](https://apidocs.document360.com/apidocs/update-an-article) |
| [Update Category](actions/update-category.md) | `PUT /v2/Categories/:categoryId` | [docs](https://apidocs.document360.com/apidocs/update-a-category) |
| [Update Category Page Content](actions/update-category-page-content.md) | `PUT /v2/Categories/:categoryId/content/:langCode` | [docs](https://apidocs.document360.com/apidocs/update-a-category-page-content-with-the-id) |
| [Update Category Type](actions/update-category-type.md) | `PUT /v2/Categories/:categoryId/updateCategoryType` | [docs](https://apidocs.document360.com/apidocs/update-the-category-type) |
