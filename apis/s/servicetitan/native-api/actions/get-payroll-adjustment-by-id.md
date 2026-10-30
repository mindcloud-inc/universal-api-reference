# Get Payroll Adjustment By Id with ServiceTitan

Retrieves a payroll adjustment from ServiceTitan by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/payroll-adjustments/:id`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Payroll Adjustment By Id](https://developer.servicetitan.io/docs/apis/tenant-payroll-v2/endpoints/PayrollAdjustments_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `employeeType` | query | `list<string>` | yes | Accepted values: `Employee`, `Technician`. |
