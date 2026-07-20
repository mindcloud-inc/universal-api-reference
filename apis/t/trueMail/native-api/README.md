# TrueMail: Native API Reference

A consolidated summary of TrueMail's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://mailcop.net/docs
- **API base URL:** `https://api.mailcop.net`

## Authentication

### API Key

Authenticate TrueMail requests with your MailCop API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mailcop.net/docs/api-overview)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Usage](actions/check-usage.md) | `GET /v1/usage` | [docs](https://mailcop.net/docs/api-usage) |
| [Create Filter](actions/create-filter.md) | `POST /v1/filters` | [docs](https://mailcop.net/docs/api-filters) |
| [Delete Filter](actions/delete-filter.md) | `DELETE /v1/filters/{{id}}` | [docs](https://mailcop.net/docs/api-filters) |
| [List Domain Filters](actions/list-domain-filters.md) | `GET /v1/filters` | [docs](https://mailcop.net/docs/api-filters) |
| [List Email Filters](actions/list-email-filters.md) | `GET /v1/filters` | [docs](https://mailcop.net/docs/api-filters) |
| [List Filters](actions/list-filters.md) | `GET /v1/filters` | [docs](https://mailcop.net/docs/api-filters) |
| [List IP Filters](actions/list-ip-filters.md) | `GET /v1/filters` | [docs](https://mailcop.net/docs/api-filters) |
| [Verify Email](actions/verify-email.md) | `POST /v1/verify` | [docs](https://mailcop.net/docs/api-verify) |
| [Verify Email MX](actions/verify-email-mx.md) | `POST /v1/verify` | [docs](https://mailcop.net/docs/api-verify) |
| [Verify Email SMTP](actions/verify-email-smtp.md) | `POST /v1/verify` | [docs](https://mailcop.net/docs/api-verify) |
