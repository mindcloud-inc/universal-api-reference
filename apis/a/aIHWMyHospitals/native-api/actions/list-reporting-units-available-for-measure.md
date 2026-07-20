# List Reporting Units Available For Measure with AIHW MyHospitals

Retrieves reporting units with data for a measure in AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/measures/{measure-code}/reporting-units-available`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Reporting Units Available For Measure](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure-code` | path | `string` | yes | The measure code. |
