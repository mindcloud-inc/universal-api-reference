# List Facility IDs with Veterans Affairs Facilities

Retrieves VA facility IDs by facility type.

## Endpoint

- **Method:** `GET`
- **Path:** `/ids`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [List Facility IDs](https://developer.va.gov/explore/api/va-facilities/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list` | no | Optional facility type filter. Accepted values: `benefits`, `cemetery`, `health`, `vet_center`. |
