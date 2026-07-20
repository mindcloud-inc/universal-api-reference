# List Reported Measures with AIHW MyHospitals

Retrieves all reported measures from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reported-measures`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Reported Measures](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure_code` | query | `string` | no | Only include reported measures matching the specified measure codes. Send multiple values as a array. |
| `reported_measure_category_code` | query | `string` | no | Only include reported measures matching the specified reported measure category codes. Send multiple values as a array. |
