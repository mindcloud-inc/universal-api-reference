# List Invoices with Avaza

Retrieves invoices from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Invoice`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Invoices](https://api.avaza.com/#!/Invoice/Invoice_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no |
| `TransactionStatusCode` | query | `string` | no |
| `IssueDateFrom` | query | `date` | no |
| `IssueDateTo` | query | `date` | no |
| `DueDateFrom` | query | `date` | no |
| `DueDateTo` | query | `date` | no |
| `CompanyIDFK` | query | `number` | no |
