# Get Employee Shifts with Paylocity

## Endpoint

- **Method:** `GET`
- **Path:** `apiHub/scheduling/v1/companies/:companyId/employees/:employeeId/shifts`
- **Base URL:** `{connection}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | breaks, segments, note |
| `filter` | query | `string` | no | - fields: startDateTime, positionKey - operators: eq, in, lt, gt, le, ge, and, or - example: startDateTime gt '2024-12-01' and startDateTime le '2025-01-25' |
| `companyId` | path | `string` | yes | — |
| `employeeId` | path | `string` | yes | — |
