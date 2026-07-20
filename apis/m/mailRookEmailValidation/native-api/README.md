# MailRook Email Validation: Native API Reference

A consolidated summary of MailRook Email Validation's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://mailrook.com/docs/api
- **API base URL:** `https://api.mailrook.com/v1`

## Authentication

### API Key

Use your MailRook API key. Requests are authenticated with an `Authorization: Bearer <API_KEY>` header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mailrook.com/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Enrich Domain](actions/enrich-domain.md) | `GET /enrich/:domain` | [docs](https://mailrook.com/docs/api) |
| [Enrich Email](actions/enrich-email.md) | `GET /enrich/:email` | [docs](https://mailrook.com/docs/api) |
| [Enrich Input](actions/enrich-input.md) | `GET /enrich/:input` | [docs](https://mailrook.com/docs/api) |
| [Get Validation Batch Results](actions/get-validation-batch-results.md) | `GET /validate/list/:listId` | [docs](https://mailrook.com/docs/api) |
| [Submit Validation Batch](actions/submit-validation-batch.md) | `POST /validate/batch` | [docs](https://mailrook.com/docs/api) |
| [Validate Email](actions/validate-email.md) | `GET /validate/:email` | [docs](https://mailrook.com/docs/api) |
