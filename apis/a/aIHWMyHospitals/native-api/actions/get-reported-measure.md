# Get Reported Measure with AIHW MyHospitals

Retrieves a reported measure from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reported-measures/{reported-measure-code}`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [Get Reported Measure](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reported-measure-code` | path | `string` | yes | The reported measure code. |
