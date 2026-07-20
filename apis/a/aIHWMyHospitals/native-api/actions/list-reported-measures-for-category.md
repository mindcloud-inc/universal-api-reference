# List Reported Measures For Category with AIHW MyHospitals

Retrieves reported measures for a category from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reported-measure-categories/{reported-measure-category-code}/reported-measures`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Reported Measures For Category](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reported-measure-category-code` | path | `string` | yes | The reported measure category code. |
