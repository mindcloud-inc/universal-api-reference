# verifi.email: Native API Reference

A consolidated summary of verifi.email's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://verifi.email/docs
- **API base URL:** `https://api.verifi.email`

## Authentication

### API Key

Authenticate verifi.email requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
token: <apiKey>
```

[Official authentication documentation](https://verifi.email/docs)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Validate Emails](actions/bulk-validate-emails.md) | `POST /v1/bulk/check` | [docs](https://verifi.email/docs) |
| [Bulk Validate Emails CSV](actions/bulk-validate-emails-csv.md) | `GET /v1/bulk/check` | [docs](https://verifi.email/docs) |
| [Check Domain Health](actions/check-domain-health.md) | `GET /v1/domain/check` | [docs](https://verifi.email/docs) |
| [Validate Email](actions/validate-email.md) | `GET /check` | [docs](https://verifi.email/docs) |
