# Get Measure with AIHW MyHospitals

Retrieves a measure from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/measures/{measure-code}`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [Get Measure](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure-code` | path | `string` | yes | The measure code. |
