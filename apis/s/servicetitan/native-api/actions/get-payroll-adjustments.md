# Get Payroll Adjustments with ServiceTitan

Retrieves payroll adjustments from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/payroll-adjustments`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Payroll Adjustments](https://developer.servicetitan.io/docs/apis/tenant-payroll-v2/endpoints/PayrollAdjustments_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeIds` | query | `string` | no | Comma-separated employee or technician IDs, such as 123,456. Send multiple values as a string separated by `,`. |
| `postedOnOrAfter` | query | `date` | no | Return adjustments posted on or after this UTC date and time. |
| `postedOnOrBefore` | query | `date` | no | Return adjustments posted on or before this UTC date and time. |
| `active` | query | `list<string>` | no | Accepted values: `Any`, `False`, `True`. |
| `createdBefore` | query | `date` | no | — |
| `createdOnOrAfter` | query | `date` | no | — |
| `modifiedBefore` | query | `date` | no | — |
| `modifiedOnOrAfter` | query | `date` | no | — |
| `includeTotal` | query | `boolean` | no | — |
| `sort` | query | `string` | no | Sort expression accepted by ServiceTitan. |
