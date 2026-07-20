# AidaForm: Native API Reference

A consolidated summary of AidaForm's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://app.swaggerhub.com/apis/aidaform/AidaForm/1.0.1
- **API base URL:** `https://api.aidaform.com/v1`

## Authentication

### API Key

Connect AidaForm with the API key from account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://aidaform.com/help/aidaform-mailchimp-zapier-integration.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://app.swaggerhub.com/apis/aidaform/AidaForm/1.0.1) |
| [List Responses](actions/list-responses.md) | `GET /forms/:formId/responses` | [docs](https://app.swaggerhub.com/apis/aidaform/AidaForm/1.0.1) |
