# List Data Items For Reporting Unit with AIHW MyHospitals

Retrieves data items for a reporting unit from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reporting-units/{reporting-unit-code}/data-items`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Data Items For Reporting Unit](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reporting-unit-code` | path | `string` | yes | The reporting unit code. |
