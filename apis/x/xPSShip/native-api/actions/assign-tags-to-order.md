# Assign Tags to Order with XPS Ship

Assigns tags to an order in XPS Ship.

## Endpoint

- **Method:** `POST`
- **Path:** `/restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId/assign-tags`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Assign Tags to Order](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/assign-tags-to-order/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationId` | path | `string` | yes | XPS Ship REST API integration ID. |
| `orderId` | path | `string` | yes | Order ID to tag. |
| `tagIds` | body | `list<string>` | yes | Array of tag IDs to assign to the order. Send multiple values as a array. |
