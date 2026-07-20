# Get Facilities by IDs with Veterans Affairs Facilities

Retrieves VA facilities by facility IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/facilities`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [Get Facilities by IDs](https://developer.va.gov/explore/api/va-facilities/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-separated facility IDs to retrieve, such as vha_688,vha_570. |
