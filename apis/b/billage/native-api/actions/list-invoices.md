# List Invoices with Billage

Retrieves invoice records from Billage by code or date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/invoices`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [List Invoices](https://app.getbillage.com/api/documentation.html#/Invoices/invoicesByParameters)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search invoices |
| `account` | query | `string` | no | Account |
| `colour` | query | `string` | no | Colour name |
| `date-from` | query | `date` | no | Date from (yyyy-MM-dd) |
| `date-to` | query | `date` | no | Date to (yyyy-MM-dd) |
| `ref` | query | `string` | no | Reference code |
| `serie` | query | `string` | no | Serie |
| `owner` | query | `string` | no | Invoice owner |
| `state` | query | `string` | no | Invoice state |
| `category` | query | `string` | no | Invoice category |
| `tags[]` | query | `array<string>` | no | Invoice tags |
| `summarized` | query | `boolean` | no | Summarized |
