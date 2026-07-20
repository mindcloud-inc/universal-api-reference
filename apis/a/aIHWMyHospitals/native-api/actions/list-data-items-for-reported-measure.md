# List Data Items For Reported Measure with AIHW MyHospitals

Retrieves data items for a reported measure from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reported-measures/{reported-measure-code}/data-items`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Data Items For Reported Measure](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reported-measure-code` | path | `string` | yes | The reported measure code. |
