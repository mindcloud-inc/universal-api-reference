# Update Order with Brightpearl

## Endpoint

- **Method:** `PATCH`
- **Path:** `/order-service/order/:orderId`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Update Order](https://api-docs.brightpearl.com/order/order/patch.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | — |
| `operations[]` | body | `array<object>` | yes | — |
| `operations[].op` | body | `list<string>` | yes | Accepted values: `remove`, `replace`. |
| `operations[].path` | body | `list<string>` | yes | Accepted values: `/delivery/deliveryDate`, `/delivery/shippingMethodId`, `/parties/billing/contactId`, `/parties/customer/contactId`, `/reference`, `/warehouseId`. |
| `operations[].value` | body | `string` | no | Required for replace; omit for remove. IDs are accepted as strings in the documented PATCH examples. |
