# Get Employee Punch Detail with Paylocity

## Endpoint

- **Method:** `GET`
- **Path:** `apiHub/time/v1/companies/:companyId/employees/:employeeId/punchDetails`
- **Base URL:** `{connection}`
- **Official documentation:** [Get Employee Punch Detail](https://developer.paylocity.com/integrations/reference/get_apihub_time_v1_companies_companyid_employees_employeeid_punchdetails)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `string` | yes |
| `employeeId` | path | `string` | yes |
| `relativeStart` | query | `string` | no |
| `relativeEnd` | query | `string` | no |
