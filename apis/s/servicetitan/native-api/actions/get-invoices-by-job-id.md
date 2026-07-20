# Get Invoices By Job Id with ServiceTitan

Retrieves invoices from ServiceTitan by job ID.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/invoices`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Invoices By Job Id](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Invoices_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobId` | query | `string` | no |
