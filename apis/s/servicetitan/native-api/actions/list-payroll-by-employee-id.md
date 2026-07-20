# List Payroll by Employee ID with ServiceTitan

Retrieves payrolls from ServiceTitan for an employee.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/employees/:employeeID/payrolls`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Payroll by Employee ID](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Return items of the specified payroll status Values: [Pending, Expired, Approved, Paid, Locked] |
| `active` | query | `list` | no | What kind of items should be returned (only active items will be returned by default) Values: [True, Any, False] |
| `employeeID` | path | `number` | no | — |
