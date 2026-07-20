# List Payroll with ServiceTitan

Retrieves payrolls from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/payrolls`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Payroll](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Return items of the specified payroll status Values: [Pending, Expired, Approved, Paid, Locked] |
| `active` | query | `list` | no | What kind of items should be returned (only active items will be returned by default) Values: [True, Any, False] |
| `pageSize` | query | `number` | no | How many records to return (50 by default) |
| `modifiedOnOrAfter` | query | `string` | no | — |
