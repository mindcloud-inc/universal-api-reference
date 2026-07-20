# List Datasets with AIHW MyHospitals

Retrieves available datasets from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/datasets`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Datasets](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure_code` | query | `string` | no | Only include datasets matching the specified measure codes. Send multiple values as a array. |
| `reported_measure_code` | query | `string` | no | Only include datasets matching the specified reported measure codes. Send multiple values as a array. |
