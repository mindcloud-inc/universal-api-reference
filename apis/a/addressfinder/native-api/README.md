# Addressfinder: Native API Reference

A consolidated summary of Addressfinder's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://addressfinder.com/au/docs/api/overview
- **OpenAPI specification:** https://addressfinder.com/au/docs/assets/files/api-d3266f757ab8175af0284fbcb3a2e99e.yaml
- **API base URL:** `https://api.addressfinder.io/api`

## Authentication

### API Key + Secret

Use your Addressfinder Portal API key and secret for server-to-server requests. The key is sent as the `key` query parameter and the secret is sent in the `Authorization` header.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `secret` · required · Your Addressfinder Portal API secret. MindCloud sends this value in the `Authorization` header for server-to-server requests.

Send these headers with each API request:

```http
Authorization: <secret>
```

[Official authentication documentation](https://addressfinder.com/au/docs/api/authentication/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get AU Address Metadata](actions/get-au-address-metadata.md) | `GET /au/address/metadata` | [docs](https://addressfinder.com/au/docs/api/au/au-address-metadata-api) |
| [Get AU Location Metadata](actions/get-au-location-metadata.md) | `GET /au/location/metadata` | [docs](https://addressfinder.com/au/docs/api/au/au-location-metadata-api) |
| [List AU Address Suggestions](actions/list-au-address-suggestions.md) | `GET /au/address/autocomplete` | [docs](https://addressfinder.com/au/docs/api/au/au-address-autocomplete-api) |
| [List AU Location Suggestions](actions/list-au-location-suggestions.md) | `GET /au/location/autocomplete` | [docs](https://addressfinder.com/au/docs/api/au/au-location-autocomplete-api) |
| [Verify AU Address](actions/verify-au-address.md) | `GET /au/address/v2/verification` | [docs](https://addressfinder.com/au/docs/api/au/au-address-verification-api) |
