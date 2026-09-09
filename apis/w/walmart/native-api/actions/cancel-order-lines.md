# Cancel Order Lines with Walmart

Cancel one or more order lines for a specific `purchaseOrderId`.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders/:purchaseOrderId/cancel`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Cancel Order Lines](https://developer.walmart.com/us-marketplace/reference/acknowledgeorders)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderId` | path | `string` | yes | Unique Walmart purchaseOrderId that identifies the purchase order. |
| `dynamicSandbox` | path | `boolean` | no | — |
| `userInputLines[].lineNumber` | body | `string` | no | Identifier of the specific order line to be cancelled. |
| `userInputLines[]` | body | `array<object>` | no | Array of objects, each specifying cancellation details for an individual order line. |
| `userInputLines[].unitOfMeasurement` | body | `list<string>` | no | Unit of measure for the status quantity (such as EACH or EA), defining how the `amount` is counted. |
| `userInputLines[].amount` | body | `number` | no | Numeric value representing how many units to be cancelled. |
| `userInputLines[].cancellationReason` | body | `list<string>` | no | Reason for cancellation. Example: 'CUSTOMER_REQUESTED_SELLER_TO_CANCEL'.  Cancellation reason should not be "CUSTOMER_REQUESTED_SELLER_TO_CANCEL" for non intent to cancel orders'  Cancellation reason should not be "SELLER_CANCEL_FRAUD_STOP_SHIPMENT" for non fraudulent orders. If you suspect fraud, contact Walmart Risk Prevention Team (MPFraudReq@customercare.walmart.com). Include PO details and reason you suspect the order. We will contact you in 2-4 hours. If your suspicion of fraud is proven, we will cancel the order and notify you.  If you select the cancellation reason as "SELLER_CANCEL_OUT_OF_STOCK", Walmart will mark the specific item as out of stock in the selected warehouse. To make the item available for sale again, please replenish its inventory. |
