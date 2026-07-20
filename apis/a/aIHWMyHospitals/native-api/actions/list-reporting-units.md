# List Reporting Units with AIHW MyHospitals

Retrieves reporting units from AIHW MyHospitals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reporting-units`
- **Base URL:** `https://myhospitalsapi.aihw.gov.au`
- **Official documentation:** [List Reporting Units](https://myhospitalsapi.aihw.gov.au/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reporting_unit_type_code` | query | `string` | no | Only include reporting units matching the specified reporting unit type codes. Send multiple values as a array. |
