# List Measures For Measure Category with AIHW MyHospitals

Retrieves measures for a measure category from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/measure-categories/{measure-category-code}/measures`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Measures For Measure Category](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure-category-code` | path | `string` | yes | The measure category code. |
