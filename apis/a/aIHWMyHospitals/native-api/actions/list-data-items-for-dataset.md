# List Data Items For Dataset with AIHW MyHospitals

Retrieves data items for a dataset from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/datasets/{dataset-id}/data-items`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Data Items For Dataset](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset-id` | path | `number` | yes | The dataset id. |
| `reporting_unit_code` | query | `string` | no | Only include data items for the specified reporting unit codes. Send multiple values as a array. |
