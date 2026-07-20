# Byteplant Address Validator: Native API Reference

A consolidated summary of Byteplant Address Validator's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.byteplant.com/address-validator/api.html
- **API base URL:** `https://api.address-validator.net`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.byteplant.com/address-validator/api.html)

## API conventions

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Address Details](actions/get-address-details.md) | `GET /api/fetch` | [docs](https://www.byteplant.com/address-validator/api.html) |
| [Search Address Suggestions](actions/search-address-suggestions.md) | `GET /api/search` | [docs](https://www.byteplant.com/address-validator/api.html) |
| [Start Bulk Address Validation](actions/start-bulk-address-validation.md) | `POST /api/bulk-verify` | [docs](https://www.byteplant.com/address-validator/api.html) |
| [Verify Address](actions/verify-address.md) | `GET /api/verify` | [docs](https://www.byteplant.com/address-validator/api.html) |
