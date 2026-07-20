# FindyMail: Native API Reference

A consolidated summary of FindyMail's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://www.findymail.com/api/
- **API base URL:** `https://app.findymail.com`

## Authentication

### API Key

Use a FindyMail API key for bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.findymail.com/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Enrich Company](actions/enrich-company.md) | `POST /api/search/company` | [docs](https://www.findymail.com/api/) |
| [Find Email](actions/find-email.md) | `POST /api/search/name` | [docs](https://www.findymail.com/api/email-finder/) |
| [Find People](actions/find-people.md) | `POST /api/search/employees` | [docs](https://www.findymail.com/api/) |
| [Find Phone Number](actions/find-phone-number.md) | `POST /api/search/phone` | [docs](https://www.findymail.com/api/) |
| [Reverse Email Lookup](actions/reverse-email-lookup.md) | `POST /api/search/reverse-email` | [docs](https://www.findymail.com/api/) |
| [Start Lead Search](actions/start-lead-search.md) | `POST /api/intellimatch/search` | [docs](https://www.findymail.com/api/) |
| [Verify Email](actions/verify-email.md) | `POST /api/verify` | [docs](https://www.findymail.com/api/email-verifier/) |
