# List Flat Data Extract with AIHW MyHospitals

Retrieves flat data for a measure category from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/flat-data-extract/{measure-category-code}`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Flat Data Extract](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measure-category-code` | path | `string` | yes | The measure category code. |
| `skip` | query | `number` | yes | The number of records to skip. |
| `top` | query | `number` | yes | The number of records to take. Must be between 1 and 1000. |
| `measure_code` | query | `string` | no | Only include data matching the specified measure codes. Send multiple values as a array. |
| `reporting_unit_code` | query | `string` | no | Only include data for the specified reporting unit codes. Send multiple values as a array. |
| `reporting_unit_type_code` | query | `string` | no | Only include data for the specified reporting unit types. Send multiple values as a array. |
| `start_date` | query | `string` | no | Only include data after this date. Use yyyy, yyyy-MM, or yyyy-MM-dd. |
| `end_date` | query | `string` | no | Only include data before this date. Use yyyy, yyyy-MM, or yyyy-MM-dd. |
