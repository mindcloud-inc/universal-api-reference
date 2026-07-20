# Address Autocomplete with Geoapify Geocode

Finds address and place suggestions in Geoapify.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/autocomplete`
- **Base URL:** `https://api.geoapify.com/v1`
- **Official documentation:** [Address Autocomplete](https://apidocs.geoapify.com/docs/geocoding/address-autocomplete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Free-form address or place text to autocomplete. |
| `type` | query | `list<string>` | no | Restrict suggestions to specific location types. Accepted values: `amenity`, `city`, `country`, `locality`, `postcode`, `state`, `street`. |
| `filter` | query | `string` | no | Restrict search area using rectangle, circle, place, or countrycode syntax. |
| `bias` | query | `string` | no | Prioritize results near a region or point. |
| `lang` | query | `string` | no | Result language using ISO 639-1 code. |
| `format` | query | `list` | no | Response format. Accepted values: `geojson`, `json`, `xml`. |
