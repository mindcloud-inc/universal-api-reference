# Postcode List with Geoapify Geocode

Retrieves a filtered list of postcodes from Geoapify.

## Endpoint

- **Method:** `GET`
- **Path:** `/postcode/list`
- **Base URL:** `https://api.geoapify.com/v1`
- **Official documentation:** [Postcode List](https://apidocs.geoapify.com/docs/postcode/#list-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Autocomplete text for postcode and locality names. |
| `filter` | query | `string` | no | Restrict search area using rectangle, circle, place, or countrycode syntax. |
| `bias` | query | `string` | no | Prioritize results near a region or point. |
| `countrycode` | query | `string` | no | ISO 3166-1 alpha-2 country code. |
| `geometry` | query | `list` | no | Geometry output style. Accepted values: `original`, `point`. |
| `lang` | query | `string` | no | Result language using ISO 639-1 code. |
| `format` | query | `list` | no | Response format. Accepted values: `geojson`, `json`, `xml`. |
