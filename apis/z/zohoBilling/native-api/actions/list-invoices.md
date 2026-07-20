# List Invoices with Zoho Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `{api_domain}/billing/v1`
- **Official documentation:** [List Invoices](https://www.zoho.com/billing/api/v1/invoices/#list-all-invoices)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_by` | query | `string` | no | Filter invoices by status, for example `Status.All`, `Status.Draft`, or `Status.Paid`. |
