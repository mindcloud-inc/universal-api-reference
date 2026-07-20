# Search Facilities by Bounding Box with Veterans Affairs Facilities

Finds VA facilities in a bounding box.

## Endpoint

- **Method:** `GET`
- **Path:** `/facilities`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [Search Facilities by Bounding Box](https://developer.va.gov/explore/api/va-facilities/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bbox[]` | query | `array<number>` | yes | Four bounding-box numbers as west longitude, south latitude, east longitude, north latitude. Send multiple values as a array. |
| `type` | query | `list` | no | Optional facility type filter. Accepted values: `benefits`, `cemetery`, `health`, `vet_center`. |
| `mobile` | query | `boolean` | no | When true, only return mobile facilities. |
| `services[]` | query | `array<string>` | no | Optional VA service identifiers to filter by. Send multiple values as a array. |
