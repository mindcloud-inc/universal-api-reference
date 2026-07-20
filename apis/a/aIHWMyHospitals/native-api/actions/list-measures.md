# List Measures with AIHW MyHospitals

Retrieves all measures from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/measures`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Measures](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure_category_code` | query | `string` | no | Only include measures matching the specified measure category codes. Send multiple values as a array. |
