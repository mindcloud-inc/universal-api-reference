# WebChange Detector: Native API Reference

A consolidated summary of WebChange Detector's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.webchangedetector.com/docs
- **OpenAPI specification:** https://api.webchangedetector.com/docs.openapi
- **API base URL:** `https://api.webchangedetector.com`

## Authentication

### API Key

Use your WebChange Detector API token from the dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.webchangedetector.com/docs)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add URLs To Group](actions/add-urls-to-group.md) | `POST /api/v2/groups/:id/add-urls` | [docs](https://api.webchangedetector.com/docs#group-POSTapi-v2-groups--id--add-urls) |
| [Create Group](actions/create-group.md) | `POST /api/v2/groups` | [docs](https://api.webchangedetector.com/docs#group-POSTapi-v2-groups) |
| [Create URL](actions/create-url.md) | `POST /api/v2/urls` | [docs](https://api.webchangedetector.com/docs#url-POSTapi-v2-urls) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v2/webhooks` | [docs](https://api.webchangedetector.com/docs#webhook-POSTapi-v2-webhooks) |
| [Delete Group](actions/delete-group.md) | `DELETE /api/v2/groups/:id` | [docs](https://api.webchangedetector.com/docs#group-DELETEapi-v2-groups--id-) |
| [Delete URL](actions/delete-url.md) | `DELETE /api/v2/urls/:id` | [docs](https://api.webchangedetector.com/docs#url-DELETEapi-v2-urls--id-) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v2/webhooks/:id` | [docs](https://api.webchangedetector.com/docs#webhook-DELETEapi-v2-webhooks--id-) |
| [Get Account](actions/get-account.md) | `GET /api/v2/account` | [docs](https://api.webchangedetector.com/docs#account-GETapi-v2-account) |
| [Get Account Stats](actions/get-account-stats.md) | `GET /api/v2/account/stats` | [docs](https://api.webchangedetector.com/docs#account-GETapi-v2-account-stats) |
| [Get Group](actions/get-group.md) | `GET /api/v2/groups/:id` | [docs](https://api.webchangedetector.com/docs#group-GETapi-v2-groups--id-) |
| [Get URL](actions/get-url.md) | `GET /api/v2/urls/:id` | [docs](https://api.webchangedetector.com/docs#url-GETapi-v2-urls--id-) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/v2/webhooks/:id` | [docs](https://api.webchangedetector.com/docs#webhook-GETapi-v2-webhooks--id-) |
| [List Group URLs](actions/list-group-urls.md) | `GET /api/v2/groups/:id/urls` | [docs](https://api.webchangedetector.com/docs#group-GETapi-v2-groups--id--urls) |
| [List Groups](actions/list-groups.md) | `GET /api/v2/groups` | [docs](https://api.webchangedetector.com/docs#group-GETapi-v2-groups) |
| [List URLs](actions/list-urls.md) | `GET /api/v2/urls` | [docs](https://api.webchangedetector.com/docs#url-GETapi-v2-urls) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v2/webhooks` | [docs](https://api.webchangedetector.com/docs#webhook-GETapi-v2-webhooks) |
| [Remove URLs From Group](actions/remove-urls-from-group.md) | `POST /api/v2/groups/:id/remove-urls` | [docs](https://api.webchangedetector.com/docs#group-POSTapi-v2-groups--id--remove-urls) |
| [Update Group](actions/update-group.md) | `PUT /api/v2/groups/:id` | [docs](https://api.webchangedetector.com/docs#group-PUTapi-v2-groups--id-) |
| [Update URL](actions/update-url.md) | `PUT /api/v2/urls/:id` | [docs](https://api.webchangedetector.com/docs#url-PUTapi-v2-urls--id-) |
| [Update Webhook](actions/update-webhook.md) | `PUT /api/v2/webhooks/:id` | [docs](https://api.webchangedetector.com/docs#webhook-PUTapi-v2-webhooks--id-) |
