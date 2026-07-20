# Forward Geocoding with Geoapify Geocode

Finds locations in Geoapify by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/search`
- **Base URL:** `https://api.geoapify.com/v1`
- **Official documentation:** [Forward Geocoding](https://apidocs.geoapify.com/docs/geocoding/forward-geocoding/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Amenity or place name |
| `text` | query | `string` | no | Free-form address or place name to geocode |
| `housenumber` | query | `string` | no | Structured address house number |
| `street` | query | `string` | no | Structured address street name |
| `postcode` | query | `string` | no | Structured address postcode or ZIP code |
| `city` | query | `string` | no | Structured address city name |
| `state` | query | `string` | no | Structured address state or region name |
| `country` | query | `string` | no | Structured address country name |
| `type` | query | `list<string>` | no | Limit results to a location type such as country, state, city, postcode, street, or amenity Accepted values: `amenity`, `city`, `country`, `locality`, `postcode`, `state`, `street`. |
| `lang` | query | `string` | no | Result language using ISO 639-1 code |
| `filter` | query | `string` | no | Restrict search area using circle, rectangle, countrycode, or place filter syntax |
| `bias` | query | `string` | no | Prioritize results near a region or point without strict filtering |
| `format` | query | `list` | no | Response format: geojson (default), json, or xml Accepted values: `geojson`, `json`, `xml`. |
