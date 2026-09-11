# Create Order PO File with Peplink

Create a customer PO File for an order.

## Endpoint

- **Method:** `POST`
- **Path:** `orders/:orderNumber/customer-po-files`
- **Base URL:** `https://portal.peplink.com/api/e/v1/cp/`
- **Official documentation:** [Create Order PO File](https://portal.peplink.com/docs/api-reference/orders/customer-po-files/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderNumber` | path | `string` | yes | — |
| `fileName` | body | `string` | yes | — |
| `fileContentInBase64` | body | `string` | yes | File content after converted into base 64. |
