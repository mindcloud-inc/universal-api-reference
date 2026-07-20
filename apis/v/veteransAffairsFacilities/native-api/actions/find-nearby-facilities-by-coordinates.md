# Find Nearby Facilities by Coordinates with Veterans Affairs Facilities

Finds nearby VA facilities by coordinates and drive time.

## Endpoint

- **Method:** `GET`
- **Path:** `/nearby`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [Find Nearby Facilities by Coordinates](https://developer.va.gov/explore/api/va-facilities/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude in WGS84 decimal degrees. |
| `long` | query | `number` | yes | Longitude in WGS84 decimal degrees. Current VA sandbox runtime expects the query key long. |
| `drive_time` | query | `list` | no | Maximum drive time in minutes. Accepted values: `10`, `20`, `30`, `40`, `50`, `60`, `70`, `80`, `90`. |
| `services[]` | query | `array<string>` | no | Optional VA service identifiers to filter by. Send multiple values as a array. |
