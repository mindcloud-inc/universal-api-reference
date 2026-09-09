# List Released Orders with Walmart

Retrieves details of all orders with line items in the "created" status.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/orders/released`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Released Orders](https://developer.walmart.com/global-marketplace/reference/getallorders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerOrderId` | query | `string` | no | — |
| `purchaseOrderId` | query | `string` | no | — |
| `sku` | query | `string` | no | — |
| `orderType` | query | `list<string>` | no | Filter by order type. Valid values are REGULAR, REPLACEMENT, PREORDER. Replacement orders appear only if replacementInfo is true. |
| `status` | query | `list<string>` | no | Status of purchase order line. Valid statuses are: Created, Acknowledged, Shipped, Delivered and Cancelled. |
| `shipNodeType` | query | `list<string>` | no | Filter by fulfillment node type. Valid values are SellerFulfilled, WFSFulfilled, and 3PLFulfilled. Default is SellerFulfilled. |
| `shippingProgramType` | query | `list<string>` | no | Filter by shipping program. Valid values are TWO_DAY or ONE_DAY. |
| `productInfo` | query | `boolean` | no | Format: `toggle`. |
| `serviceInfo` | query | `boolean` | no | Format: `toggle`. |
| `replacementInfo` | query | `boolean` | no | Include replacement order attributes (originalCustomerOrderID, orderType) in the response when true. Valid values are true or false. Format: `toggle`. |
| `createdStartDate` | query | `string` | no | — |
| `createdEndDate` | query | `string` | no | — |
| `fromExpectedShipDate` | query | `string` | no | — |
| `toExpectedShipDate` | query | `string` | no | — |
| `lastModifiedStartDate` | query | `string` | no | — |
| `lastModifiedEndDate` | query | `string` | no | — |
| `dynamicSandbox` | path | `boolean` | no | - When Toggled Off and credential is set to 'Sandbox' - this request will return a static list of released Walmart Sandbox Orders. - Toggle on to fetch released Orders from your Dynamic Sandbox ( created via the SImulations API. ) |
