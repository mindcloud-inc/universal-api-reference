# Create Order Fulfillment with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [Create Order Fulfillment](https://shopify.dev/docs/api/admin-graphql/latest/mutations/fulfillmentCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | GraphQL variables for the fulfillment. |
| `variables.fulfillment` | body | `object` | no | The fulfillment details sent to Shopify. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[]` | body | `array<object>` | yes | One or more fulfillment orders assigned to the same Shopify order and location. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderId` | body | `string` | yes | Shopify Fulfillment Order GID. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[]` | body | `array<object>` | yes | Add each confirmed Fulfillment Order line item and quantity to ship. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].id` | body | `string` | yes | Shopify Fulfillment Order Line Item GID, not the ordinary Order Line Item GID. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].quantity` | body | `number` | yes | Quantity of this fulfillment-order line item to fulfill. |
| `variables.fulfillment.trackingInfo` | body | `object` | no | Tracking information for the shipment. |
| `variables.fulfillment.trackingInfo.company` | body | `string` | no | Carrier name. A Shopify-supported carrier can enable automatic tracking URLs. |
| `variables.fulfillment.trackingInfo.number` | body | `string` | yes | — |
| `variables.fulfillment.trackingInfo.url` | body | `string` | no | Optional complete tracking URL. |
| `variables.fulfillment.notifyCustomer` | body | `boolean` | no | Whether Shopify should email the customer about the fulfillment. Defaults to false. |
| `variables.message` | body | `string` | no | Optional message associated with the fulfillment. |
