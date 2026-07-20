# Put Order with XPS Ship

Creates or updates an order in XPS Ship.

## Endpoint

- **Method:** `PUT`
- **Path:** `/restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Put Order](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/put-order/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationId` | path | `string` | yes | XPS Ship REST API integration ID. |
| `orderId` | path | `string` | yes | Unique order ID, matching the orderId in the request body. |
| `orderId` | body | `string` | yes | Required order ID in the JSON body; must match the URL order ID. |
| `orderDate` | body | `string` | yes | Date the order was placed. |
| `orderNumber` | body | `string` | yes | Invoice number of the order, or null. |
| `fulfillmentStatus` | body | `string` | yes | One of pending, fulfilled, or partial. |
| `shippingService` | body | `string` | yes | Name of shipping service associated with order, or null. |
| `shippingTotal` | body | `string` | yes | Amount the customer paid for shipping, or null. |
| `weightUnit` | body | `string` | yes | Weight unit, lb or kg, or null. |
| `dimUnit` | body | `string` | yes | Dimension unit, in or cm, or null. |
| `dueByDate` | body | `string` | yes | Date by which the order must be fulfilled, or null. |
| `orderGroup` | body | `string` | yes | Group for multi-user shipping, or null. |
| `sender` | body | `object` | yes | Required sender address object. |
| `receiver` | body | `object` | yes | Required receiver address object. |
| `items` | body | `list<object>` | yes | Order item array, or null. Send multiple values as a array. |
| `packages` | body | `list<object>` | yes | Package array, or null. Send multiple values as a array. |
| `shipperReference` | body | `string` | no | Optional reference text to show on the shipping label. |
| `shipperReference2` | body | `string` | no | Optional second reference field for the label when supported by the carrier. |
| `contentDescription` | body | `string` | no | Optional content description of the shipment. |
| `returnTo` | body | `object` | no | Optional return-to address object. |
