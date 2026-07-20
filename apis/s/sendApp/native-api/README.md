# SendApp: Native API Reference

A consolidated summary of SendApp's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://official.sendapp.cloud/apiv3/
- **API base URL:** `https://official.sendapp.cloud/apiv3`

## Authentication

### API Key

Authenticate SendApp requests with the account access token passed as the shared access_token query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://official.sendapp.cloud/apiv3/)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://official.sendapp.cloud/apiv3/) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://official.sendapp.cloud/apiv3/) |
| [Send Media Message](actions/send-media-message.md) | `GET /send/media` | [docs](https://official.sendapp.cloud/apiv3/) |
| [Send Template Message](actions/send-template-message.md) | `GET /send/template` | [docs](https://official.sendapp.cloud/apiv3/) |
| [Send Text Message](actions/send-text-message.md) | `GET /send/text` | [docs](https://official.sendapp.cloud/apiv3/) |
