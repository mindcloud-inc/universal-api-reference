# Register Order with Zakeke

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/order`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Register Order](https://docs.zakeke.com/docs/API/orders-API#7-register-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderCode` | body | `string` | yes | Unique identifier of the order on the ecommerce. |
| `orderDate` | body | `string` | yes | Order date in ISO 8601 format. |
| `customerCode` | body | `string` | no | Registered customer identifier from the ecommerce system. |
| `visitorCode` | body | `string` | no | Visitor identifier from the ecommerce system when there is no registered customer. |
| `sessionID` | body | `string` | no | The ecommerce session identifier. |
| `details[].orderDetailCode` | body | `string` | yes | The ID on your system for the customized-product line item. |
| `total` | body | `number` | yes | The total order amount in the base currency set in Zakeke API settings. |
| `details` | body | `list<object>` | no | List of customized product details. |
| `details[].sku` | body | `string` | yes | Unique identifier that the ordered customized product has in ecommerce. |
| `details[].designID` | body | `string` | yes | Unique design identifier provided by Zakeke. |
| `details[].modelUnitPrice` | body | `number` | yes | Product unit price without the design price. |
| `details[].designUnitPrice` | body | `number` | yes | Unit price applied to customization. |
| `details[].quantity` | body | `number` | yes | Quantity of products ordered. |
| `details[].designModificationID` | body | `string` | no | Identifier assigned by Zakeke for a specific Names and Numbers or bulk-variation instance. |
| `compositionDetails[].orderDetailCode` | body | `string` | yes | The ID on your system for the configured-product line item. |
| `compositionDetails` | body | `list<object>` | no | List of configured product details. |
| `compositionDetails[].composition` | body | `string` | yes | The product configuration identifier for the configured product that the line item belongs to. |
| `compositionDetails[].unitPrice` | body | `number` | yes | The unit price of the configured product including configuration price after discounts. |
| `compositionDetails[].quantity` | body | `number` | yes | The number of configured products that were purchased. |
