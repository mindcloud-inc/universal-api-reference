# Get Invoices with ServiceTitan

Retrieves invoices from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/invoices`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Invoices](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Invoices_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `invoicedOnOrAfter` | query | `string` | no | — |
| `invoicedOnBefore` | query | `string` | no | — |
| `ids` | query | `number` | no | — |
| `orderBy` | query | `string` | no | — |
| `orderByDirection` | query | `string` | no | Order direction of the retuned list of invoices. Values of "desc" or "descending" will order the list in descending order, otherwise the list will be ordered in ascending order. |
| `customerId` | query | `string` | no | — |
| `totalLess` | query | `number` | no | — |
| `batchId` | query | `number` | no | Batch ID associated with invoices. |
| `batchNumber` | query | `number` | no | Batch number associated with invoices. |
| `shortcutDimension1Code` | query | `string` | no | — |
| `number` | query | `string` | no | — |
| `active` | query | `string` | no | — |
| `jobId` | query | `string` | no | — |
| `createdBefore` | query | `string` | no | — |
| `totalGreater` | query | `number` | no | Retrieve all invoices with a total greater than or equal to the input value. |
| `statuses` | query | `list` | no | — |
| `createdOnOrAfter` | query | `string` | no | Return items created on or after certain date/time (in UTC) |
