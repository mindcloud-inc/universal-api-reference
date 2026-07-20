# Unassign Tags from Order with XPS Ship

Unassigns tags from an order in XPS Ship.

## Endpoint

- **Method:** `POST`
- **Path:** `/restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId/unassign-tags`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Unassign Tags from Order](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/unassign-tags-from-order/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationId` | path | `string` | yes | XPS Ship REST API integration ID. |
| `orderId` | path | `string` | yes | Order ID to untag. |
| `tagIds` | body | `list<string>` | yes | Array of tag IDs to unassign from the order. Send multiple values as a array. |
