# List Payments with Avaza

Retrieves payments from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Payment`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Payments](https://api.avaza.com/#!/Payment/Payment_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceTransactionID` | query | `number` | no | Filter for Payments that have at least one allocation against a given Invoice Transaction ID |
| `UpdatedAfter` | query | `date` | no | Filter for Payments updated after a given date |
