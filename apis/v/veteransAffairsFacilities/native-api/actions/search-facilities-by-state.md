# Search Facilities by State with Veterans Affairs Facilities

Finds VA facilities in a state.

## Endpoint

- **Method:** `GET`
- **Path:** `/facilities`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [Search Facilities by State](https://developer.va.gov/explore/api/va-facilities/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | yes | Two-letter state code to search within. Maximum length: 2. |
| `type` | query | `list` | no | Optional facility type filter. Accepted values: `benefits`, `cemetery`, `health`, `vet_center`. |
| `mobile` | query | `boolean` | no | When true, only return mobile facilities. |
| `services[]` | query | `array<string>` | no | Optional VA service identifiers to filter by. Send multiple values as a array. |
