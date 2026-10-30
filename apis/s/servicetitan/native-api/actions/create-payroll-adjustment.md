# Create Payroll Adjustment with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `payroll/v2/tenant/{tenant}/payroll-adjustments`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Create Payroll Adjustment](https://developer.servicetitan.io/docs/apis/tenant-payroll-v2/endpoints/PayrollAdjustments_Create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeType` | body | `list<string>` | yes | Accepted values: `Employee`, `Technician`. |
| `employeeId` | body | `number` | yes | ID of the employee or technician selected by Employee Type. |
| `postedOn` | body | `date` | yes | Date and time the adjustment is posted, in UTC. |
| `amount` | body | `number` | no | — |
| `memo` | body | `string` | no | — |
| `activityCodeId` | body | `number` | no | — |
| `invoiceId` | body | `list<number>` | no | — |
| `businessUnitId` | body | `list<number>` | no | — |
| `hours` | body | `number` | no | — |
| `rate` | body | `number` | no | — |
| `quantity` | body | `number` | no | — |
