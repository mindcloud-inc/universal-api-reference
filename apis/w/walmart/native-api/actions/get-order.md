# Get Order with Walmart

Retrieves an order detail for a specific purchaseOrderId

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/orders/:purchaseOrderId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Order](https://developer.walmart.com/global-marketplace/reference/getallorders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productInfo` | query | `boolean` | no | Format: `toggle`. |
| `purchaseOrderId` | path | `string` | yes | Unique Walmart purchaseOrderId that identifies the purchase order. |
| `dynamicSandbox` | path | `boolean` | no | - When Toggled Off and credential is set to 'Sandbox' - this request will return a static Walmart Sandbox Order. - Toggle on to fetch an Order from your Dynamic Sandbox ( created via the SImulations API. ) |
| `replacementInfo` | query | `boolean` | no | Include replacement order attributes (originalCustomerOrderID, orderType) in the response when true. Valid values are true or false. Format: `toggle`. |
