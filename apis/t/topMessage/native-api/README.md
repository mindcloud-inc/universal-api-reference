# TopMessage: Native API Reference

A consolidated summary of TopMessage's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://topmessage.com/documentation-api/send-message
- **API base URL:** `https://api.topmessage.com`

## Authentication

### API Key

Authenticate TopMessage requests with an API key sent in the X-TopMessage-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-TopMessage-Key: <apiKey>
```

[Official authentication documentation](https://topmessage.com/documentation-api/get-message)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Message By ID](actions/get-message-by-id.md) | `GET /v1/messages/:Id` | [docs](https://topmessage.com/documentation-api/get-message) |
| [List Messages](actions/list-messages.md) | `GET /v1/messages` | [docs](https://topmessage.com/documentation-api/get-message) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Send Scheduled SMS](actions/send-scheduled-sms.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Send Simple SMS](actions/send-simple-sms.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Send SMS Template Message](actions/send-sms-template-message.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Send SMS With Shortened Links](actions/send-sms-with-shortened-links.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Send Verification SMS](actions/send-verification-sms.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Send WhatsApp Free-form Reply](actions/send-whats-app-free-form-reply.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Send WhatsApp Template Message](actions/send-whats-app-template-message.md) | `POST /v1/messages` | [docs](https://topmessage.com/documentation-api/send-message) |
| [Verify Message Code](actions/verify-message-code.md) | `GET /v1/messages` | [docs](https://topmessage.com/documentation-api/get-message) |
