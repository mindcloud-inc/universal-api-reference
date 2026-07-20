# Create Invoice for Customer with Billwerkplus

Creates an invoice for a Billwerkplus customer.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/:handle/invoice`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Create Invoice for Customer](https://docs.frisbii.com/reference/createcustomerinvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Customer handle. |
| `handle` | body | `string` | yes | Unique invoice handle. |
| `order_lines[]` | body | `array<object>` | yes | Invoice order lines. |
