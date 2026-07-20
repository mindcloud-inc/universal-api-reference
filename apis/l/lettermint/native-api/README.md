# Lettermint: Native API Reference

A consolidated summary of Lettermint's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://lettermint.co/docs/api-reference/sending
- **API base URL:** `https://api.lettermint.co/v1`

## Authentication

### Project Sending API Token

Authenticate with a Lettermint project sending token using the x-lettermint-token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-lettermint-token: <apiKey>
```

[Official authentication documentation](https://lettermint.co/docs/api-reference/sending)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ping API](actions/ping-api.md) | `GET /ping` | [docs](https://lettermint.co/docs/api-reference/sending/generic#ping-the-api) |
| [Send Email](actions/send-email.md) | `POST /send` | [docs](https://lettermint.co/docs/api-reference/sending/send#send-an-email) |
| [Send Multiple Emails in a Batch](actions/send-multiple-emails-in-a-batch.md) | `POST /send/batch` | [docs](https://lettermint.co/docs/api-reference/sending/send#send-multiple-emails-in-a-batch) |
