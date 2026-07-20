# Geoapify Geocode: Native API Reference

A consolidated summary of Geoapify Geocode's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.geoapify.com/docs
- **OpenAPI specification:** https://raw.githubusercontent.com/geoapify/geoapify-openapi-specs/refs/heads/main/api-specs/geocoding/forward_geocoding.yaml
- **API base URL:** `https://api.geoapify.com/v1`

## Authentication

### API Key

Geoapify API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.geoapify.com/docs/geocoding/forward-geocoding/)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apiKey` | query | `string` | no | Geoapify API key query parameter mapped from credentials.apiKey |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (minimum 0).

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Address Autocomplete](actions/address-autocomplete.md) | `GET /geocode/autocomplete` | [docs](https://apidocs.geoapify.com/docs/geocoding/address-autocomplete/) |
| [Forward Geocoding](actions/forward-geocoding.md) | `GET /geocode/search` | [docs](https://apidocs.geoapify.com/docs/geocoding/forward-geocoding/) |
| [IP Geolocation](actions/ip-geolocation.md) | `GET /ipinfo` | [docs](https://apidocs.geoapify.com/docs/ip-geolocation/) |
| [Postcode List](actions/postcode-list.md) | `GET /postcode/list` | [docs](https://apidocs.geoapify.com/docs/postcode/#list-api) |
| [Postcode Search](actions/postcode-search.md) | `GET /postcode/search` | [docs](https://apidocs.geoapify.com/docs/postcode/#search-api) |
| [Reverse Geocoding](actions/reverse-geocoding.md) | `GET /geocode/reverse` | [docs](https://apidocs.geoapify.com/docs/geocoding/reverse-geocoding/) |
