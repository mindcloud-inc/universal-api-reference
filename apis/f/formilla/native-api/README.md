# Formilla: Native API Reference

A consolidated summary of Formilla's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://blog.formilla.com/integrate-customer-data-with-the-formilla-rest-api/
- **API base URL:** `https://api.formilla.com/api`

## Authentication

### API Key

Use your Formilla REST API secure token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://blog.formilla.com/use-formilla-javascript-rest-apis-securely/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create or Update Contact (Email Required)](actions/upsert-contact-by-email.md) | `POST /contacts` | [docs](https://blog.formilla.com/integrate-customer-data-with-the-formilla-rest-api/) |
| [Create or Update Contact (User ID Required)](actions/upsert-contact-by-user-id.md) | `POST /contacts` | [docs](https://blog.formilla.com/integrate-customer-data-with-the-formilla-rest-api/) |
