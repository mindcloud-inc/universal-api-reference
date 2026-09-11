# Update Technician Payroll Settings with ServiceTitan

## Endpoint

- **Method:** `PUT`
- **Path:** `payroll/v2/tenant/{tenant}/technicians/:technician/payroll-settings`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Technician Payroll Settings](https://developer.servicetitan.io/docs/apis/tenant-payroll-v2/endpoints/PayrollSettings_UpdateTechnicianPayrollSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `technician` | path | `number` | yes | The ServiceTitan technician ID. |
| `externalPayrollId` | body | `string` | no | Optional identifier from the external payroll system. |
| `hourlyRate` | body | `number` | yes | Hourly rate for the technician payroll settings. |
| `managerId` | body | `number` | no | Optional manager employee ID. |
| `hireDate` | body | `date` | no | Optional hire date and time. |
| `isIncludedInPayroll` | body | `boolean` | no | Whether the technician is included in payroll processing. |
| `customFields[]` | body | `array<object>` | no | Optional custom payroll-field values to update for the technician. |
| `customFields[].typeId` | body | `number` | yes | Custom payroll field definition ID. |
| `customFields[].value` | body | `string` | no | Optional custom payroll field value. |
