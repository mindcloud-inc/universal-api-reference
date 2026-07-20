# List Bricks Available For Reporting Unit Type with AIHW MyHospitals

Retrieves available bricks by reporting unit for a type in AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reporting-unit-types/{reporting-unit-type-code}/bricks-available`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Bricks Available For Reporting Unit Type](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reporting-unit-type-code` | path | `string` | yes | The reporting unit type code. |
