# Get Vendor Bills with ServiceTitan

Retrieves vendor bills from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/inventory-bills`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Vendor Bills](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Invoices_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `invoicedOnOrAfter` | query | `string` | no | — |
| `ids` | query | `string` | no | — |
| `orderBy` | query | `string` | no | — |
| `orderByDirection` | query | `string` | no | Order direction of the retuned list of invoices. Values of "desc" or "descending" will order the list in descending order, otherwise the list will be ordered in ascending order. |
| `customerId` | query | `string` | no | — |
| `totalLess` | query | `number` | no | — |
