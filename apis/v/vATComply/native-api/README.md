# VAT Comply: Native API Reference

A consolidated summary of VAT Comply's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://www.vatcomply.com
- **OpenAPI specification:** https://api.vatcomply.com/docs/openapi.json
- **API base URL:** `https://api.vatcomply.com`

## Authentication

### No Authentication

Public API; no credentials required.

This API does not require request authentication.

[Official authentication documentation](https://www.vatcomply.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Health](actions/check-api-health.md) | `GET /health` | [docs](https://api.vatcomply.com/docs) |
| [Check API Readiness](actions/check-api-readiness.md) | `GET /ready` | [docs](https://api.vatcomply.com/docs) |
| [Geolocate Request IP](actions/geolocate-request-ip.md) | `GET /geolocate` | [docs](https://api.vatcomply.com/docs) |
| [Get API Information](actions/get-api-information.md) | `GET /` | [docs](https://api.vatcomply.com/docs) |
| [Get Exchange Rates](actions/get-exchange-rates.md) | `GET /rates` | [docs](https://www.vatcomply.com/api/rates/) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://www.vatcomply.com/api/countries/) |
| [List Currencies](actions/list-currencies.md) | `GET /currencies` | [docs](https://www.vatcomply.com/api/currencies/) |
| [List VAT Rates](actions/list-vat-rates.md) | `GET /vat_rates` | [docs](https://www.vatcomply.com/api/vat-rates/) |
| [Validate IBAN](actions/validate-iban.md) | `GET /iban` | [docs](https://api.vatcomply.com/docs) |
| [Validate VAT Number](actions/validate-vat-number.md) | `GET /vat` | [docs](https://api.vatcomply.com/docs) |
