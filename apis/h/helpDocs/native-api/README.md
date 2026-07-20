# HelpDocs: Native API Reference

A consolidated summary of HelpDocs's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.helpdocs.io/
- **API base URL:** `https://api.helpdocs.io/v1`

## Authentication

### API Key

Connect with a HelpDocs API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.helpdocs.io/article/caacxCUso6-authenticating-api-requests)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `skip` in the query string as the record offset.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | `POST /article` | [docs](https://apidocs.helpdocs.io/article/8Y2t6NVxeU-creating-an-article) |
| [Create Category](actions/create-category.md) | `POST /category` | [docs](https://apidocs.helpdocs.io/category/9UJDUIt9h0-categories) |
| [Create Clip](actions/create-clip.md) | `POST /clip` | [docs](https://apidocs.helpdocs.io/article/jpaw9kp9wg-creating-a-clip) |
| [Create Group](actions/create-group.md) | `POST /account/group` | [docs](https://apidocs.helpdocs.io/article/b80vu2xkz6-creating-a-group) |
| [Delete Article](actions/delete-article.md) | `DELETE /article/:article_id` | [docs](https://apidocs.helpdocs.io/article/0iyvUUh7py-deleting-an-article) |
| [Delete Category](actions/delete-category.md) | `DELETE /category/:category_id` | [docs](https://apidocs.helpdocs.io/article/Hw8fVbXt1V-deleting-a-category) |
| [Delete Clip](actions/delete-clip.md) | `DELETE /clip/:clip_id` | [docs](https://apidocs.helpdocs.io/category/n1i20sex9q-clips) |
| [Delete Group](actions/delete-group.md) | `DELETE /account/group/:group_id` | [docs](https://apidocs.helpdocs.io/article/5z6h2zwa29-deleting-a-group) |
| [Generate Chatbot Source Page](actions/generate-chatbot-source-page.md) | `GET /article` | [docs](https://apidocs.helpdocs.io/article/4xha228dwf-generating-a-chatbot-source-page) |
| [Get Aggregate Time Series Data](actions/get-aggregate-time-series-data.md) | `GET /stats/graph` | [docs](https://apidocs.helpdocs.io/article/tt4hqtxwss-aggregate-time-series-data) |
| [Get Article](actions/get-article.md) | `GET /article/:article_id` | [docs](https://apidocs.helpdocs.io/category/Z83io6YtSs-articles) |
| [Get Article Feedback](actions/get-article-feedback.md) | `GET /stats/feedback` | [docs](https://apidocs.helpdocs.io/article/xvypxgyg1x-article-feedback) |
| [Get Article Versions](actions/get-article-versions.md) | `GET /article/:article_id/versions` | [docs](https://apidocs.helpdocs.io/article/c3svl5hvb2-getting-article-versions) |
| [Get Category](actions/get-category.md) | `GET /category/:category_id` | [docs](https://apidocs.helpdocs.io/category/9UJDUIt9h0-categories) |
| [Get Clip](actions/get-clip.md) | `GET /clip/:clip_id` | [docs](https://apidocs.helpdocs.io/category/n1i20sex9q-clips) |
| [Get Search Terms](actions/get-search-terms.md) | `GET /stats/search` | [docs](https://apidocs.helpdocs.io/article/uzu96zl0nr-search-terms) |
| [Get Top Articles](actions/get-top-articles.md) | `GET /stats/article` | [docs](https://apidocs.helpdocs.io/article/6xq7bnm6w2-top-articles) |
| [List Articles](actions/list-articles.md) | `GET /article` | [docs](https://apidocs.helpdocs.io/article/OqvaxRMHgN-getting-articles) |
| [List Categories](actions/list-categories.md) | `GET /category` | [docs](https://apidocs.helpdocs.io/article/W7M0gESe8R-getting-categories) |
| [List Groups](actions/list-groups.md) | `GET /account/group` | [docs](https://apidocs.helpdocs.io/category/bwwio42u7z-user-permission-groups) |
| [Search Articles](actions/search-articles.md) | `GET /search` | [docs](https://apidocs.helpdocs.io/article/If1U9NNUpT-searching-for-articles) |
| [Update Article](actions/update-article.md) | `PATCH /article/:article_id` | [docs](https://apidocs.helpdocs.io/category/Z83io6YtSs-articles) |
| [Update Category](actions/update-category.md) | `PATCH /category/:category_id` | [docs](https://apidocs.helpdocs.io/article/9f9mMkb0od-updating-a-category) |
| [Update Clip](actions/update-clip.md) | `PATCH /clip/:clip_id` | [docs](https://apidocs.helpdocs.io/article/yl1k6865rt-updating-a-clip) |
| [Update Group](actions/update-group.md) | `PATCH /account/group/:group_id` | [docs](https://apidocs.helpdocs.io/article/r5k7g79ici-updating-a-group) |
