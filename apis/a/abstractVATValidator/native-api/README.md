# Abstract VAT Validator: Native API Reference

A consolidated summary of Abstract VAT Validator's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.abstractapi.com/api/vat-validation
- **API base URL:** `https://vat.abstractapi.com/v1`

## Authentication

### API Key

Use an Abstract VAT Validation API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.abstractapi.com/api/vat-validation)

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate VAT](actions/calculate-vat.md) | `GET /calculate` | [docs](https://abstractapi-vat.mintlify.app/vat-validation/calculate) |
| [Get VAT Categories](actions/get-vat-categories.md) | `GET /categories` | [docs](https://abstractapi-vat.mintlify.app/vat-validation/categories) |
| [Validate VAT Number](actions/validate-vat-number.md) | `GET /validate` | [docs](https://abstractapi-vat.mintlify.app/vat-validation/validate) |
