# List Invoices with Metronome

Retrieves invoices from Metronome.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/invoices`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [List Invoices](https://docs.metronome.com/api-reference/invoices/list-invoices)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | path | `string` | yes |
