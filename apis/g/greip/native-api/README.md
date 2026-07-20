# Greip - Fraud Prevention: Native API Reference

A consolidated summary of Greip - Fraud Prevention's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.greip.io/introduction
- **API base URL:** `https://greipapi.com`

## Authentication

### API Key

Connect Greip with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.greip.io/authentication)

## API conventions

Response data is read from `data`.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete User Data](actions/delete-user-data.md) | `DELETE /account/users/delete` | [docs](https://docs.greip.io/api-reference/endpoint/account/users/delete) |
| [Get ASN Lookup](actions/get-asn-lookup.md) | `GET /lookup/asn` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/asn) |
| [Get BIN/IIN Lookup](actions/get-bin-iin-lookup.md) | `GET /lookup/bin` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/bin) |
| [Get Bulk IP Lookup](actions/get-bulk-ip-lookup.md) | `GET /lookup/ip/bulk` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/bulk-ip) |
| [Get Country Lookup](actions/get-country-lookup.md) | `GET /lookup/country` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/country) |
| [Get Domain Lookup](actions/get-domain-lookup.md) | `GET /lookup/domain` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/domain) |
| [Get Email Scoring](actions/get-email-scoring.md) | `GET /scoring/email` | [docs](https://docs.greip.io/api-reference/endpoint/scoring/email) |
| [Get Free IP](actions/get-free-ip.md) | `GET /ip` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/free-get-ip-method) |
| [Get IBAN Lookup](actions/get-iban-lookup.md) | `GET /lookup/iban` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/iban) |
| [Get IP Geolocation](actions/get-ip-geolocation.md) | `GET /geoip` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/geoip) |
| [Get IP Lookup](actions/get-ip-lookup.md) | `GET /lookup/ip` | [docs](https://docs.greip.io/api-reference/endpoint/data-lookup/ip) |
| [Get IP Reputation](actions/get-ip-reputation.md) | `GET /lookup/ip/threats` | [docs](https://docs.greip.io/api-reference/endpoint/scoring/ip-reputation) |
| [Get Phone Number Scoring](actions/get-phone-number-scoring.md) | `GET /scoring/phone` | [docs](https://docs.greip.io/api-reference/endpoint/scoring/phone) |
| [Get Profanity Detection](actions/get-profanity-detection.md) | `GET /scoring/profanity` | [docs](https://docs.greip.io/api-reference/endpoint/scoring/profanity) |
| [Run Payment Fraud Detection](actions/run-payment-fraud-detection.md) | `POST /scoring/payment` | [docs](https://docs.greip.io/api-reference/endpoint/scoring/payment) |
