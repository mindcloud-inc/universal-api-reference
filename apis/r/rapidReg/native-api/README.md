# RapidReg: Native API Reference

A consolidated summary of RapidReg's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://rapidreg.com/developers
- **API base URL:** `https://rapidreg.com`

## Authentication

### API Key

Authenticate RapidReg requests with an API key passed in the api request field.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.rapidreg.com/developers/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `POST /api/v1/get/account` | [docs](https://rapidreg.com/developers#dev-account) |
| [List Brands](actions/list-brands.md) | `POST /api/v1/get/brands` | [docs](https://rapidreg.com/developers#dev-brands) |
| [List Items](actions/list-items.md) | `POST /api/v1/get/items` | [docs](https://rapidreg.com/developers#dev-items) |
| [List Registrations](actions/list-registrations.md) | `POST /api/v1/get/registrations` | [docs](https://rapidreg.com/developers#dev-reg) |
