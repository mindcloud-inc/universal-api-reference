# ipdata.co: Native API Reference

A consolidated summary of ipdata.co's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://docs.ipdata.co
- **API base URL:** `https://api.ipdata.co`

## Authentication

### API Key

Authenticate ipdata requests with an API key in the api-key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ipdata.co/docs/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Caller IP Basic ASN](actions/get-caller-ip-basic-asn.md) | `GET /asn` | [docs](https://docs.ipdata.co/docs/asn-data) |
| [Get Caller IP Carrier](actions/get-caller-ip-carrier.md) | `GET /carrier` | [docs](https://docs.ipdata.co/docs/mobile-carrier-detection) |
| [Get Caller IP Company](actions/get-caller-ip-company.md) | `GET /` | [docs](https://docs.ipdata.co/docs/ip-to-company-api) |
| [Get Caller IP Coordinates](actions/get-caller-ip-coordinates.md) | `GET /` | [docs](https://docs.ipdata.co/docs/geolocation) |
| [Get Caller IP Country](actions/get-caller-ip-country.md) | `GET /` | [docs](https://docs.ipdata.co/docs/filtering-response-fields) |
| [Get Caller IP Country Metadata](actions/get-caller-ip-country-metadata.md) | `GET /` | [docs](https://docs.ipdata.co/docs/all-response-fields) |
| [Get Caller IP Currency](actions/get-caller-ip-currency.md) | `GET /currency` | [docs](https://docs.ipdata.co/docs/all-response-fields) |
| [Get Caller IP Details](actions/get-caller-ip-details.md) | `GET /` | [docs](https://docs.ipdata.co/docs/getting-started) |
| [Get Caller IP Languages](actions/get-caller-ip-languages.md) | `GET /` | [docs](https://docs.ipdata.co/docs/filtering-response-fields) |
| [Get Caller IP Region And Postal](actions/get-caller-ip-region-and-postal.md) | `GET /` | [docs](https://docs.ipdata.co/docs/geolocation) |
| [Get Caller IP Selected Fields](actions/get-caller-ip-selected-fields.md) | `GET /` | [docs](https://docs.ipdata.co/docs/filtering-response-fields) |
| [Get Caller IP Threat Summary](actions/get-caller-ip-threat-summary.md) | `GET /threat` | [docs](https://docs.ipdata.co/docs/proxy-tor-and-threat-detection) |
| [Get Caller IP Time Zone](actions/get-caller-ip-time-zone.md) | `GET /time_zone` | [docs](https://docs.ipdata.co/docs/all-response-fields) |
| [Get IP Basic ASN](actions/get-ip-basic-asn.md) | `GET /:ip/asn` | [docs](https://docs.ipdata.co/docs/asn-data) |
| [Get IP Blocklists](actions/get-ip-blocklists.md) | `GET /:ip/threat` | [docs](https://docs.ipdata.co/docs/blocklists) |
| [Get IP Carrier](actions/get-ip-carrier.md) | `GET /:ip/carrier` | [docs](https://docs.ipdata.co/docs/mobile-carrier-detection) |
| [Get IP Company](actions/get-ip-company.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/ip-to-company-api) |
| [Get IP Coordinates](actions/get-ip-coordinates.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/geolocation) |
| [Get IP Country](actions/get-ip-country.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/filtering-response-fields) |
| [Get IP Country Metadata](actions/get-ip-country-metadata.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/all-response-fields) |
| [Get IP Currency](actions/get-ip-currency.md) | `GET /:ip/currency` | [docs](https://docs.ipdata.co/docs/all-response-fields) |
| [Get IP Details](actions/get-ip-details.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/getting-started) |
| [Get IP Languages](actions/get-ip-languages.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/filtering-response-fields) |
| [Get IP Region And Postal](actions/get-ip-region-and-postal.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/geolocation) |
| [Get IP Reputation Scores](actions/get-ip-reputation-scores.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/ip-reputation-api) |
| [Get IP Selected Fields](actions/get-ip-selected-fields.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/filtering-response-fields) |
| [Get IP Threat Summary](actions/get-ip-threat-summary.md) | `GET /:ip/threat` | [docs](https://docs.ipdata.co/docs/proxy-tor-and-threat-detection) |
| [Get IP Time Zone](actions/get-ip-time-zone.md) | `GET /:ip/time_zone` | [docs](https://docs.ipdata.co/docs/all-response-fields) |
| [Get IP VPN Detection](actions/get-ipvpn-detection.md) | `GET /:ip` | [docs](https://docs.ipdata.co/docs/vpn-detection) |
