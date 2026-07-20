# CNPJá: Native API Reference

A consolidated summary of CNPJá's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://cnpja.com/en/api/reference
- **API base URL:** `https://api.cnpja.com`

## Authentication

### API Key

Authenticate CNPJá requests with the API key from your CNPJá account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://cnpja.com/en/api/reference)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Office by Tax ID](actions/get-office-by-tax-id.md) | `GET /office/:taxId` | [docs](https://cnpja.com/en/api/reference) |
| [Get Office Geocoding](actions/get-office-geocoding.md) | `GET /office/:taxId` | [docs](https://cnpja.com/en/api) |
| [Get Office State Registrations](actions/get-office-state-registrations.md) | `GET /office/:taxId` | [docs](https://cnpja.com/en/api) |
| [Get Office SUFRAMA](actions/get-office-suframa.md) | `GET /office/:taxId` | [docs](https://cnpja.com/en/api) |
| [Get Office Tax Regime](actions/get-office-tax-regime.md) | `GET /office/:taxId` | [docs](https://cnpja.com/en/api) |
