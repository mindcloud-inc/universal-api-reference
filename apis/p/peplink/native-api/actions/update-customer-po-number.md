# Update customer PO number with Peplink

Update customer PO number for an order.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/:orderNumber/customer-po-number`
- **Base URL:** `https://portal.peplink.com/api/e/v1/cp/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderNumber` | path | `string` | yes |
| `customerPoNumber` | body | `string` | yes |
