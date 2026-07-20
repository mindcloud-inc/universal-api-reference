# talkSpirit: Native API Reference

A consolidated summary of talkSpirit's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://talkspirit.github.io/
- **API base URL:** `https://webhook.talkspirit.com`

## Authentication

### Incoming Webhook URL

Connect talkSpirit using the full incoming webhook URL.

### Credentials

- **Webhook URL:** `webhookUrl` · required · Paste the full talkSpirit incoming webhook URL.

[Official authentication documentation](https://talkspirit.github.io/docs/create-incoming-webhook/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Post](actions/send-post.md) | `POST {{credentials.webhookUrl}}` | [docs](https://talkspirit.github.io/docs/incoming-webhooks/#sending-posts) |
