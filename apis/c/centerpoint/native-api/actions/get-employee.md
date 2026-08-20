# Get Employee with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `employees/:EMPLOYEE_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Employee](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/employees/{EMPLOYEE_ID}GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EMPLOYEE_ID` | path | `string` | yes | The employee id to retrieve. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `include` | query | `string` | no | Optional include query parameter. |
