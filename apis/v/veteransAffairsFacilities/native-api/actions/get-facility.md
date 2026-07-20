# Get Facility with Veterans Affairs Facilities

Retrieves a VA facility by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/facilities/:facilityId`
- **Base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`
- **Official documentation:** [Get Facility](https://developer.va.gov/explore/api/va-facilities/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `facilityId` | path | `string` | yes | Facility ID in the form prefix_station, such as vha_688. |
