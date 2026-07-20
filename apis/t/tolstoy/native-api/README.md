# Tolstoy: Native API Reference

A consolidated summary of Tolstoy's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developers.gotolstoy.com/welcome
- **API base URL:** `https://api.gotolstoy.com`

## Authentication

### API Key

Connect Tolstoy with an API Key from Tolstoy Settings > My workspace.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.gotolstoy.com/en/articles/5772218-where-do-i-see-my-tolstoy-ids)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | `POST /webhooks/` | [docs](https://developers.gotolstoy.com/webhooks/add-webhook) |
| [Create Project](actions/create-project.md) | `POST /projects/` | [docs](https://developers.gotolstoy.com/api-reference/create-project) |
| [Create Video by URL](actions/create-video-by-url.md) | `POST /videos/video` | [docs](https://developers.gotolstoy.com/api-reference/create-video-by-url) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://developers.gotolstoy.com/webhooks/delete-webhook) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://developers.gotolstoy.com/api-reference/get-project) |
| [List Videos](actions/list-videos.md) | `GET /videos/videos` | [docs](https://developers.gotolstoy.com/api-reference/list-videos) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/` | [docs](https://developers.gotolstoy.com/webhooks/list-webhooks) |
