# API Labz: Native API Reference

A consolidated summary of API Labz's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://apilabz.apidog.io/
- **API base URL:** `https://hub.apilabz.com`

## Authentication

### API Key

Use your API Labz token as the bearer value for Authorization header requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apilabz.apidog.io/)

## API conventions

Response data is read from `response`.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Domain Lookup](actions/domain-lookup.md) | `POST /module/131` | [docs](https://apilabz.apidog.io/domain-lookup-15128896e0) |
| [Domain WHOIS Lookup](actions/domain-whois-lookup.md) | `POST /module/614` | [docs](https://apilabz.apidog.io/domain-whois-lookup-15128905e0) |
| [Email Validator](actions/email-validator.md) | `POST /module/111` | [docs](https://apilabz.apidog.io/email-validator-15128887e0) |
| [IBAN Validator](actions/iban-validator.md) | `POST /module/113` | [docs](https://apilabz.apidog.io/iban-validator-15128889e0) |
| [VAT Validator](actions/vat-validator.md) | `POST /module/114` | [docs](https://apilabz.apidog.io/vat-validator-15128890e0) |
