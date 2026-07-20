# Rowform: Native API Reference

A consolidated summary of Rowform's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://help.rowform.io/api-reference
- **API base URL:** `https://app.rowform.io`

## Authentication

### API Key

Authenticate Rowform Zapier API requests with a Rowform organization API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://help.rowform.io/api-reference)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Form Responses](actions/get-form-responses.md) | `GET /api/zapier/responses` | [docs](https://help.rowform.io/api-reference#get-form-responses) |
| [List Forms](actions/list-forms.md) | `GET /api/zapier/forms` | [docs](https://help.rowform.io/api-reference#list-forms) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/zapier/hooks` | [docs](https://help.rowform.io/api-reference#list-webhooks) |
| [Subscribe Webhook](actions/subscribe-webhook.md) | `POST /api/zapier/hooks` | [docs](https://help.rowform.io/api-reference#subscribe-webhook) |
| [Test Authentication](actions/test-authentication.md) | `GET /api/zapier/auth` | [docs](https://help.rowform.io/api-reference#test-authentication) |
| [Unsubscribe Webhook](actions/unsubscribe-webhook.md) | `DELETE /api/zapier/hooks` | [docs](https://help.rowform.io/api-reference#unsubscribe-webhook) |
