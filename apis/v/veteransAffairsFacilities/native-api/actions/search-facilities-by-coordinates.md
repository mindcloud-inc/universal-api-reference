# Search Facilities by Coordinates with Veterans Affairs Facilities

Finds VA facilities near latitude and longitude coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/facilities`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [Search Facilities by Coordinates](https://developer.va.gov/explore/api/va-facilities/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude in WGS84 decimal degrees. |
| `long` | query | `number` | yes | Longitude in WGS84 decimal degrees. |
| `type` | query | `list` | no | Optional facility type filter. Accepted values: `benefits`, `cemetery`, `health`, `vet_center`. |
| `mobile` | query | `boolean` | no | When true, only return mobile facilities. |
| `services[]` | query | `array<string>` | no | Optional VA service identifiers to filter by. Send multiple values as a array. |
