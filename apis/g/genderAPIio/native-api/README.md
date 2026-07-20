# GenderAPI.io: Native API Reference

A consolidated summary of GenderAPI.io's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.genderapi.io/api-documentation
- **API base URL:** `https://api.genderapi.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.genderapi.io/docs-authentication)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Gender by Email](actions/get-gender-by-email.md) | `POST /api/email` | [docs](https://www.genderapi.io/docs-gender-from-email-single) |
| [Get Gender by Email Batch](actions/get-gender-by-email-batch.md) | `POST /api/email/multi/country` | [docs](https://www.genderapi.io/docs-gender-from-email-multiple) |
| [Get Gender by Email (GET)](actions/get-gender-by-email-get.md) | `GET /api/email` | [docs](https://www.genderapi.io/docs-gender-from-email-single) |
| [Get Gender by Name](actions/get-gender-by-name.md) | `POST /api` | [docs](https://www.genderapi.io/docs-gender-from-name-single) |
| [Get Gender by Name Batch](actions/get-gender-by-name-batch.md) | `POST /api/name/multi/country` | [docs](https://www.genderapi.io/docs-gender-from-name-multiple) |
| [Get Gender by Name (GET)](actions/get-gender-by-name-get.md) | `GET /api` | [docs](https://www.genderapi.io/docs-gender-from-name-single) |
| [Get Gender by Username](actions/get-gender-by-username.md) | `POST /api/username` | [docs](https://www.genderapi.io/docs-gender-from-username-single) |
| [Get Gender by Username Batch](actions/get-gender-by-username-batch.md) | `POST /api/username/multi/country` | [docs](https://www.genderapi.io/docs-gender-from-username-multiple) |
| [Get Gender by Username (GET)](actions/get-gender-by-username-get.md) | `GET /api/username` | [docs](https://www.genderapi.io/docs-gender-from-username-single) |
| [Get Remaining Credits](actions/get-remaining-credits.md) | `GET /api/remaining` | [docs](https://www.genderapi.io/docs-usage-and-quota) |
| [Validate Phone Number](actions/validate-phone-number.md) | `POST /api/phone` | [docs](https://www.genderapi.io/docs-phone-validation-formatter-api) |
| [Validate Phone Number (GET)](actions/validate-phone-number-get.md) | `GET /api/phone` | [docs](https://www.genderapi.io/docs-phone-validation-formatter-api) |
