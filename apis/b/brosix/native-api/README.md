# Brosix: Native API Reference

A consolidated summary of Brosix's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.brosix.com/notifications-api/
- **API base URL:** `https://box-n2.brosix.com/api/v1`

## Authentication

### API Key

Connect Brosix Notifications API with a channel-scoped API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.brosix.com/notifications-api/)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | `POST /message/send/` | [docs](https://help.brosix.com/notifications-api/) |
