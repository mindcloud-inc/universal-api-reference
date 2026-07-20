# Get Reported Measure Category with AIHW MyHospitals

Retrieves a reported measure category from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reported-measure-categories/{reported-measure-category-code}`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [Get Reported Measure Category](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reported-measure-category-code` | path | `string` | yes | The reported measure category code. |
