# List Orders with Rithum DSCO

Lists orders in Rithum DSCO.

## Endpoint

- **Method:** `GET`
- **Path:** `order/page`
- **Base URL:** `https://api.dsco.io/api/v3`
- **Official documentation:** [List Orders](https://api.dsco.io/doc/v3/reference/#tag/Order/operation/getOrders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scrollId` | query | `string` | no | Pagination scroll identifier returned by a prior DSCO orders page response. |
| `consumerOrderNumber` | query | `string` | no | Filter orders by consumer order number. |
| `ordersCreatedSince` | query | `date` | no | Filter to orders created since this timestamp. |
| `ordersUpdatedSince` | query | `date` | no | Filter to orders updated since this timestamp. |
| `until` | query | `date` | no | Upper timestamp bound for the order query. |
| `status` | query | `string` | no | Filter orders by DSCO order status. |
| `includeTestOrders` | query | `boolean` | no | Whether DSCO should include test orders in the response. |
| `returnedOnly` | query | `boolean` | no | Whether to return only orders with returns. |
| `ordersPerPage` | query | `number` | no | Maximum number of orders to return in the page. |
| `lifecycle` | query | `string` | no | Filter orders by lifecycle. |
