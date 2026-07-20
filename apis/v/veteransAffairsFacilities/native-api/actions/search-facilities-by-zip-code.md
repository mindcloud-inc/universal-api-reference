# Search Facilities by ZIP Code with Veterans Affairs Facilities

Finds VA facilities near a ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/facilities`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [Search Facilities by ZIP Code](https://developer.va.gov/explore/api/va-facilities/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | query | `string` | yes | Five-digit or ZIP+4 code to search near. |
| `type` | query | `list` | no | Optional facility type filter. Accepted values: `benefits`, `cemetery`, `health`, `vet_center`. |
| `mobile` | query | `boolean` | no | When true, only return mobile facilities. |
| `services[]` | query | `array<string>` | no | Optional VA service identifiers to filter by. Send multiple values as a array. |
