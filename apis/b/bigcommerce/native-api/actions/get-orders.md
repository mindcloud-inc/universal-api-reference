# Get Orders with BigCommerce

Gets all orders

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/orders`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`
- **Official documentation:** [Get Orders](https://developer.bigcommerce.com/docs/rest-management/orders#get-all-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status_id` | query | `string` | no | Status Identifier of the orders you want |
| `min_date_modified` | query | `string` | no | Minimum date the order was modified in RFC-2822 or ISO-8601.  RFC-2822: Thu, 20 Apr 2017 11:32:00 -0400  ISO-8601: 2017-04-20T11:32:00.000-04:00 |
| `max_date_modified` | query | `string` | no | — |
| `min_date_created` | query | `string` | no | Minimum date the order was created in RFC-2822 or ISO-8601. RFC-2822: Thu, 20 Apr 2017 11:32:00 -0400 ISO-8601: 2017-04-20T11:32:00.000-04:00 |
| `max_date_created` | query | `string` | no | — |
| `min_id` | query | `string` | no | The minimum order ID. |
| `max_id` | query | `string` | no | — |
| `external_order_id` | query | `string` | no | The order ID in another system, such as the Amazon Order ID if this is an Amazon order. |
| `channel_id` | query | `string` | no | The channel ID of the sales channel the shopper used to place the order. |
| `include` | query | `string` | no | Allowed: consignments \| consignments.line_items \| fees |
