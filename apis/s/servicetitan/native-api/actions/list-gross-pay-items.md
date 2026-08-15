# List Gross Pay Items with ServiceTitan

Retrieves gross pay items from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/gross-pay-items`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Gross Pay Items](https://developer.servicetitan.io/docs/apis/tenant-payroll-v2/endpoints/GrossPayItems_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no |
| `employeeId` | query | `string` | no |
| `payrollIds` | query | `string` | no |
