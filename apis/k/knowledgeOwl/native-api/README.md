# KnowledgeOwl: Native API Reference

A consolidated summary of KnowledgeOwl's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://support.knowledgeowl.com/help/use-api
- **OpenAPI specification:** https://support.knowledgeowl.com/app/image/id/695315989d79a7be7201613f/n/knowledgeowl-external.yaml
- **API base URL:** `https://app.knowledgeowl.com/api/head`

## Authentication

### Basic Auth

KnowledgeOwl API uses HTTP Basic auth with the API key as the username and any value as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.knowledgeowl.com/help/use-api)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | `POST /article.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Create Category](actions/create-category.md) | `POST /category.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Create File](actions/create-file.md) | `POST /file.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Create Reader](actions/create-reader.md) | `POST /reader.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Create Tag](actions/create-tag.md) | `POST /tag.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhook.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Delete Article](actions/delete-article.md) | `DELETE /article/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Delete Category](actions/delete-category.md) | `DELETE /category/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Delete File](actions/delete-file.md) | `DELETE /file/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Delete Reader](actions/delete-reader.md) | `DELETE /reader/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tag/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /webhook/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Get Article](actions/get-article.md) | `GET /article/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Get Category](actions/get-category.md) | `GET /category/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Get File](actions/get-file.md) | `GET /file/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Get Reader](actions/get-reader.md) | `GET /reader/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Get Tag](actions/get-tag.md) | `GET /tag/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /webhook/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [List Articles](actions/list-articles.md) | `GET /article.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [List Categories](actions/list-categories.md) | `GET /category.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [List Files](actions/list-files.md) | `GET /file.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [List Readers](actions/list-readers.md) | `GET /reader.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [List Tags](actions/list-tags.md) | `GET /tag.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhook.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Replace File Contents](actions/replace-file-contents.md) | `POST /file/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Update Article](actions/update-article.md) | `PUT /article/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Update Category](actions/update-category.md) | `PUT /category/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Update File](actions/update-file.md) | `PUT /file/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Update Reader](actions/update-reader.md) | `PUT /reader/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Update Tag](actions/update-tag.md) | `PUT /tag/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | `PUT /webhook/:id.json` | [docs](https://support.knowledgeowl.com/help/api-endpoint-reference) |
