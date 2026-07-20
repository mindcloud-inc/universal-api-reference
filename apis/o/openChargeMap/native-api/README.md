# Open Charge Map: Native API Reference

A consolidated summary of Open Charge Map's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.openchargemap.org/develop/api
- **OpenAPI specification:** https://raw.githubusercontent.com/openchargemap/ocm-docs/master/Model/schema/ocm-openapi-spec.yaml
- **API base URL:** `https://api.openchargemap.io/v3`

## Authentication

### API Key

Use an Open Charge Map API key for API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://community.openchargemap.org/t/api-keys-are-now-required/161)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Open Charge Map/1.0` |

Responses from this API use JSON.

## Pagination

Use `maxresults` in the query string to set the page size (default 5; minimum 1).

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Charging Location By ID](actions/get-charging-location-by-id.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [Get Core Reference Data](actions/get-core-reference-data.md) | `GET /referencedata` | [docs](https://www.openchargemap.org/develop/api) |
| [Get OpenAPI Definition](actions/get-open-api-definition.md) | `GET /openapi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-openapi) |
| [Get Reference Data By Country ID](actions/get-reference-data-by-country-id.md) | `GET /referencedata` | [docs](https://www.openchargemap.org/develop/api#/operations/get-referencedata) |
| [List Charging Locations Along Route](actions/list-charging-locations-along-route.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Charging Locations By Country Code](actions/list-charging-locations-by-country-code.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Charging Locations By Country ID](actions/list-charging-locations-by-country-id.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Charging Locations In Bounding Box](actions/list-charging-locations-in-bounding-box.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Charging Locations In Polygon](actions/list-charging-locations-in-polygon.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Locations After ID](actions/list-locations-after-id.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Locations By Connection Type](actions/list-locations-by-connection-type.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Locations By Data Provider](actions/list-locations-by-data-provider.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Locations By Operator](actions/list-locations-by-operator.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Locations By Status Type](actions/list-locations-by-status-type.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Locations By Usage Type](actions/list-locations-by-usage-type.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Locations With Comments](actions/list-locations-with-comments.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Nearby Charging Locations](actions/list-nearby-charging-locations.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Open Data Locations](actions/list-open-data-locations.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [List Recently Modified Locations](actions/list-recently-modified-locations.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
| [Search Charging Locations](actions/search-charging-locations.md) | `GET /poi` | [docs](https://www.openchargemap.org/develop/api#/operations/get-poi) |
