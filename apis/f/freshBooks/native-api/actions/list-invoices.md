# List Invoices with FreshBooks

Retrieves invoices from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/invoices/invoices`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [List Invoices](https://www.freshbooks.com/api/invoices)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
