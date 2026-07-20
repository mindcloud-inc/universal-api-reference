# Get Order with Amazon Seller

Retrieves an order from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `orders/2026-01-01/orders/:orderId`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Order](https://developer-docs.amazon.com/sp-api/reference/getorder-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | An Amazon-defined order identifier. |
| `includedData` | query | `list<string>` | no | Specify which datasets to include in the response. - BUYER	Information about the buyer who purchased the order. - RECIPIENT	Information about the recipient to whom the order is delivered. - PROCEEDS	The revenue and financial breakdown for the order and order items. - EXPENSE	The cost information applied to the order and order items. - PROMOTION	The discount and promotional offer details applied to the order and order items. - CANCELLATION	Cancellation information applied to the order and order items. - FULFILLMENT	Information about how this order and order items are processed and shipped. - PACKAGES	Shipping packages and tracking information. Send multiple values as a array. |
