# no2bounce: Native API Reference

A consolidated summary of no2bounce's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.no2bounce.com/api-documentation
- **API base URL:** `https://connect.no2bounce.com/v2`

## Authentication

### API Token

Use a no2bounce API token generated from the API page in your no2bounce account.

### Credentials

- **API Token:** `apiKey` · required · Paste the API token generated from the no2bounce API page.

Send these headers with each API request:

```http
apitoken: <apiKey>
```

[Official authentication documentation](https://www.no2bounce.com/api-documentation)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Bulk Validation Status](actions/get-bulk-validation-status.md) | `GET /n2b_validate_bulk` | [docs](https://www.no2bounce.com/api-documentation#validating-api-request) |
| [Submit Bulk Validation](actions/submit-bulk-validation.md) | `POST /n2b_validate_bulk` | [docs](https://www.no2bounce.com/api-documentation#making-api-request) |
