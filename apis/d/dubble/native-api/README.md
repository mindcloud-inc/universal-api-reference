# Dubble: Native API Reference

A consolidated summary of Dubble's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://dubble.readme.io
- **API base URL:** `https://api.dubble.so/v1`

## Authentication

### API Key

Use a Dubble API token to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.dubble.so/en/articles/11-dubble-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Guide to Collection](actions/add-guide-to-collection.md) | `PUT /guides/:guideId/collections/:collectionId` | [docs](https://dubble.readme.io/reference/addguidetocollection) |
| [Create Collection](actions/create-collection.md) | `POST /collections` | [docs](https://dubble.readme.io/reference/createcollection) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://dubble.readme.io/reference/post_webhooks) |
| [Create Webhook for Collection](actions/create-webhook-for-collection.md) | `POST /webhooks/:collectionId` | [docs](https://dubble.readme.io/reference/post_webhooks-collectionid) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /collections/:collectionId` | [docs](https://dubble.readme.io/reference/deletecollection) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://dubble.readme.io/reference/deletewebhook) |
| [Get Guide](actions/get-guide.md) | `GET /guides/:guideId` | [docs](https://dubble.readme.io/reference/getguide) |
| [Get Guide as HTML](actions/get-guide-as-html.md) | `GET /guides/:guideId/html` | [docs](https://dubble.readme.io/reference/getguidehtml) |
| [Get Guide as Markdown](actions/get-guide-as-markdown.md) | `GET /guides/:guideId/markdown` | [docs](https://dubble.readme.io/reference/getguidemarkdown) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://dubble.readme.io/reference/getcollections) |
| [List Guides](actions/list-guides.md) | `GET /guides` | [docs](https://dubble.readme.io/reference/getguides) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://dubble.readme.io/reference/getwebhooks) |
| [Remove Guide from Collection](actions/remove-guide-from-collection.md) | `DELETE /guides/:guideId/collections/:collectionId` | [docs](https://dubble.readme.io/reference/removeguidefromcollection) |
| [Update Collection](actions/update-collection.md) | `PUT /collections/:collectionId` | [docs](https://dubble.readme.io/reference/updatecollection) |
| [Update Guide](actions/update-guide.md) | `PUT /guides/:guideId` | [docs](https://dubble.readme.io/reference/updateguide) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:webhookId` | [docs](https://dubble.readme.io/reference/updatewebhook) |
