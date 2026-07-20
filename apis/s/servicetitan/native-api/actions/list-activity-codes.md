# List Activity Codes with ServiceTitan

Retrieves activity codes from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/tenant/{tenant}/activity-codes`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Activity Codes](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `list` | no | What kind of items should be returned (only active items will be returned by default) Values: [True, Any, False] |
| `pageSize` | query | `number` | no | How many records to return (50 by default) |
