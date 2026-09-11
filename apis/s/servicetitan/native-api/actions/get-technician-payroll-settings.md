# Get Technician Payroll Settings with ServiceTitan

Retrieves payroll settings from ServiceTitan for a technician.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/technicians/:technician/payroll-settings`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Technician Payroll Settings](https://developer.servicetitan.io/docs/apis/tenant-payroll-v2/endpoints/PayrollSettings_GetTechnicianPayrollSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `technician` | path | `number` | yes | The technician identifier. |
