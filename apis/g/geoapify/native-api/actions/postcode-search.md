# Postcode Search with Geoapify Geocode

Finds postcodes in Geoapify by location or value.

## Endpoint

- **Method:** `GET`
- **Path:** `/postcode/search`
- **Base URL:** `https://api.geoapify.com/v1`
- **Official documentation:** [Postcode Search](https://apidocs.geoapify.com/docs/postcode/#search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postcode` | query | `string` | no | Postcode to look up. |
| `lat` | query | `number` | no | Latitude for nearest postcode search. |
| `lon` | query | `number` | no | Longitude for nearest postcode search. |
| `countrycode` | query | `string` | no | ISO 3166-1 alpha-2 country code. |
| `geometry` | query | `list` | no | Geometry output style. Accepted values: `original`, `point`. |
| `lang` | query | `string` | no | Result language using ISO 639-1 code. |
| `format` | query | `list` | no | Response format. Accepted values: `geojson`, `json`, `xml`. |
