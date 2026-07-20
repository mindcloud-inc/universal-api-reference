# List AU Location Suggestions with Addressfinder

Finds Australian location suggestions in Addressfinder by partial query.

## Endpoint

- **Method:** `GET`
- **Path:** `/au/location/autocomplete`
- **Base URL:** `https://api.addressfinder.io/api`
- **Official documentation:** [List AU Location Suggestions](https://addressfinder.com/au/docs/api/au/au-location-autocomplete-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The query string to match against locations. |
| `location_types` | query | `string` | no | Comma-separated location types to allow: street, locality, or state. |
| `state_codes` | query | `string` | no | Filter results by state or territory codes. |
| `domain` | query | `string` | no | Registered domain used for activity monitoring. |
| `max` | query | `number` | no | Maximum number of results to return. |
| `highlight` | query | `number` | no | Set to 1 to include highlighted matching terms in the response. |
| `format` | query | `string` | no | Response format. |
