# Disparo PRO: Native API Reference

A consolidated summary of Disparo PRO's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://painel.disparopro.com.br/docs/rcs
- **OpenAPI specification:** https://gateway.disparopro.com.br/rcs/docs-json
- **API base URL:** `https://gateway.disparopro.com.br/rcs`

## Authentication

### API Key

Use the integration token generated in Disparo PRO to authenticate RCS API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
token: <apiKey>
```

[Official authentication documentation](https://disparopro.com.br/api-rcs-como-utilizar/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `items`. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Template](actions/activate-template.md) | `PATCH /template/activate/:id` | [docs](https://painel.disparopro.com.br/docs/rcs) |
| [Create Template](actions/create-template.md) | `POST /template` | [docs](https://painel.disparopro.com.br/docs/rcs) |
| [Deactivate Template](actions/deactivate-template.md) | `PATCH /template/deactivate/:id` | [docs](https://painel.disparopro.com.br/docs/rcs) |
| [Get Template](actions/get-template.md) | `GET /template/:id` | [docs](https://painel.disparopro.com.br/docs/rcs) |
| [List Templates](actions/list-templates.md) | `GET /template` | [docs](https://painel.disparopro.com.br/docs/rcs) |
| [Send Basic RCS Message](actions/send-basic-rcs-message.md) | `POST /message/basic` | [docs](https://painel.disparopro.com.br/docs/rcs) |
| [Send Single RCS Message](actions/send-single-rcs-message.md) | `POST /message/single` | [docs](https://painel.disparopro.com.br/docs/rcs) |
