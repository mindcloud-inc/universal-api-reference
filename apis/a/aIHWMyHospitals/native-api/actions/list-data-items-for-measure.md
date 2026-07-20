# List Data Items For Measure with AIHW MyHospitals

Retrieves data items for a measure from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/measures/{measure-code}/data-items`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Data Items For Measure](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure-code` | path | `string` | yes | The measure code. |
