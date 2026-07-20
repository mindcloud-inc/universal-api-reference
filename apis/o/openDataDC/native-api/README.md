# Open Data DC: Native API Reference

A consolidated summary of Open Data DC's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json
- **OpenAPI specification:** https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json
- **API base URL:** `https://datagate.dc.gov/mar/open`

## Authentication

### API Key

DC MAR 2 API key sent as the `apikey` query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · DC MAR 2 API key. This is the only credential secret; requests send it through the shared `apikey` query parameter.

[Official authentication documentation](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Address](actions/autocomplete-address.md) | `GET /api/v2.2/autocomplete/:address` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Autocomplete Address From Body](actions/autocomplete-address-from-body.md) | `POST /api/v2.2/autocomplete` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Autocomplete Address With POST](actions/autocomplete-address-with-post.md) | `POST /api/v2.2/autocomplete/:address` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Location Batch](actions/create-location-batch.md) | `POST /api/v2.2/locationbatch` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Location Batch With Path Options](actions/create-location-batch-with-path-options.md) | `POST /api/v2.2/locationbatch/:address_separator/:chunkSequnce_separator/:parallel` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Location By Address And Zones From Body](actions/create-location-by-address-and-zones-from-body.md) | `POST /api/v2.2/locations/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Location By Address From Body](actions/create-location-by-address-from-body.md) | `POST /api/v2.2/locations/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Location By Address With Zones](actions/create-location-by-address-with-zones.md) | `POST /api/v2.2/locations/:address/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Locations By Coordinates](actions/create-locations-by-coordinates.md) | `POST /api/v2.2/locations/:latlong/:distance/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Locations By Coordinates From Body](actions/create-locations-by-coordinates-from-body.md) | `POST /api/v2.2/locations/:distance/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Locations By Coordinates With Zones](actions/create-locations-by-coordinates-with-zones.md) | `POST /api/v2.2/locations/:latlong/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Nearest Locations By Coordinates](actions/create-nearest-locations-by-coordinates.md) | `POST /api/v2.2/locations/:latlong` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Nearest Locations By Coordinates With Count](actions/create-nearest-locations-by-coordinates-with-count.md) | `POST /api/v2.2/locations/:latlong/:count/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Nearest Locations From Body](actions/create-nearest-locations-from-body.md) | `POST /api/v2.2/locations/:count/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create SSL Lookup](actions/create-ssl-lookup.md) | `POST /api/v2.2/ssls` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create SSL Lookup By Identifier](actions/create-ssl-lookup-by-identifier.md) | `POST /api/v2.2/ssls/:ssl` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Unit Lookup](actions/create-unit-lookup.md) | `POST /api/v2.2/units` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Units Lookup By MAR ID](actions/create-units-lookup-by-mar-id.md) | `POST /api/v2.2/units/:marid` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Units Lookup By MAR ID And Type](actions/create-units-lookup-by-mar-id-and-type.md) | `POST /api/v2.2/units/:marid/:type` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Create Zone Lookup](actions/create-zone-lookup.md) | `POST /api/v2.2/zone/:zone` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Location Batch](actions/get-location-batch.md) | `GET /api/v2.2/locationbatch/:address_base64/:address_separator/:chunkSequnce_separator/:parallel` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Location Batch With Query Options](actions/get-location-batch-with-query-options.md) | `GET /api/v2.2/locationbatch/:address_base64` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Location By Address](actions/get-location-by-address.md) | `GET /api/v2.2/locations/:address` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Location By Address With Zones](actions/get-location-by-address-with-zones.md) | `GET /api/v2.2/locations/:address/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Locations By Coordinates](actions/get-locations-by-coordinates.md) | `GET /api/v2.2/locations/:latlong/:distance/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Locations By Coordinates With Zones](actions/get-locations-by-coordinates-with-zones.md) | `GET /api/v2.2/locations/:latlong/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Nearest Locations By Coordinates](actions/get-nearest-locations-by-coordinates.md) | `GET /api/v2.2/locations/:latlong` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Nearest Locations By Coordinates With Count](actions/get-nearest-locations-by-coordinates-with-count.md) | `GET /api/v2.2/locations/:latlong/:count/:zones/:geo` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get SSL By Identifier](actions/get-ssl-by-identifier.md) | `GET /api/v2.2/ssls/:ssl` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Units By MAR ID](actions/get-units-by-mar-id.md) | `GET /api/v2.2/units/:marid` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Units By MAR ID And Type](actions/get-units-by-mar-id-and-type.md) | `GET /api/v2.2/units/:marid/:type` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Get Zone](actions/get-zone.md) | `GET /api/v2.2/zone/:zone` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Search SSLs](actions/search-ssls.md) | `GET /api/v2.2/ssls` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
| [Search Units](actions/search-units.md) | `GET /api/v2.2/units` | [docs](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json) |
