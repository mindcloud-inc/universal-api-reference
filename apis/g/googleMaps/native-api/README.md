# Google Maps: Native API Reference

A consolidated summary of Google Maps's API configuration and 3 documented operations.

## Authentication

### Custom

### Credentials

- **API Key:** `apiKey` · optional
- **Project ID:** `projectID` · optional

Send these headers with each API request:

```http
X-Goog-Api-Key: <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Geocode Address](actions/geocode-address.md) | `GET https://maps.googleapis.com/maps/api/geocode/json` | [docs](https://developers.google.com/maps/documentation/geocoding/requests-geocoding) |
| [Get Route Matrix](actions/get-route-matrix.md) | `POST https://routes.googleapis.com/distanceMatrix/v2:computeRouteMatrix` | [docs](https://developers.google.com/maps/documentation/routes/compute_route_matrix) |
| [Validate Address](actions/validate-address.md) | `POST https://addressvalidation.googleapis.com/v1::validateAddress?alt=json&fields=*` | [docs](https://developers.google.com/maps/documentation/address-validation/reference/rest/v1/TopLevel/validateAddress) |
