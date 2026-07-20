# ProveSource: Native API Reference

A consolidated summary of ProveSource's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.provesrc.com/en/collections/2021450-webhooks
- **API base URL:** `https://api.provesrc.com`

## Authentication

### API Key

Connect with a ProveSource API key from Settings > Account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.provesrc.com/en/articles/3485750-where-do-i-find-my-api-key)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Webhook Event](actions/send-webhook-event.md) | `POST /webhooks/track/:webhookId` | [docs](https://help.provesrc.com/en/articles/3474258-setup-a-custom-webhook) |
