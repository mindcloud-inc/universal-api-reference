# Get AU Location Metadata with Addressfinder

Retrieves metadata for an Australian location from Addressfinder.

## Endpoint

- **Method:** `GET`
- **Path:** `/au/location/metadata`
- **Base URL:** `https://api.addressfinder.io/api`
- **Official documentation:** [Get AU Location Metadata](https://addressfinder.com/au/docs/api/au/au-location-metadata-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Unique location identifier obtained from the AU Location Autocomplete API. |
| `domain` | query | `string` | no | Registered domain used for activity monitoring. |
| `format` | query | `string` | no | Response format. |
