# Email List Validation: Native API Reference

A consolidated summary of Email List Validation's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.emaillistvalidation.com/
- **API base URL:** `https://app.emaillistvalidation.com`

## Authentication

### API Key

Use an Email List Validation API key from the dashboard API section.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.emaillistvalidation.com/en/article/18-api-authentication)

## API conventions

Responses from this API use plain text.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Verify Email Address](actions/verify-email-address.md) | `GET /api/verifEmail` | [docs](https://help.emaillistvalidation.com/en/article/25-api-authentication) |
