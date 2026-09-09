# Get Label Details with Walmart

Retrieves all label details generated for a purchase order id.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/shipping/labels/purchase-orders/:purchaseOrderId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Label Details](https://developer.walmart.com/us-marketplace/reference/getlabel#:~:text=Utilities-,Labels%20detail%20by%20purchase%20order%20id,-GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderId` | path | `string` | yes | A unique `purchaseOrderId` to retrieve label details for. |
