# List Bricks Available For Reporting Unit with AIHW MyHospitals

Retrieves available brick codes for a reporting unit in AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reporting-units/{reporting-unit-code}/bricks-available`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Bricks Available For Reporting Unit](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reporting-unit-code` | path | `string` | yes | The reporting unit code. |
