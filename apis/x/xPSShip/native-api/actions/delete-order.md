# Delete Order with XPS Ship

Deletes an existing order from XPS Ship.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Delete Order](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/delete-order/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationId` | path | `string` | yes | XPS Ship REST API integration ID. |
| `orderId` | path | `string` | yes | Unique order ID to delete. |
