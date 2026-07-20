# List Orders with Order Desk

Retrieves orders from Order Desk.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [List Orders](https://apidocs.orderdesk.com/?shell=#get-multiple-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | query | `string` | no | Filter to a specific folder ID or comma-separated folder IDs. |
| `folder_name` | query | `string` | no | Filter to a folder by exact folder name. |
| `source_id` | query | `string` | no | Filter to a specific source ID. |
| `source_name` | query | `string` | no | Filter to a specific source name. |
| `search_start_date` | query | `string` | no | UTC start date for added orders, in Order Desk date-time format. |
| `search_end_date` | query | `string` | no | UTC end date for added orders, in Order Desk date-time format. |
| `modified_start_date` | query | `string` | no | UTC start date for modified orders, in Order Desk date-time format. |
| `modified_end_date` | query | `string` | no | UTC end date for modified orders, in Order Desk date-time format. |
| `email` | query | `string` | no | Filter by customer email address. |
| `customer_id` | query | `string` | no | Filter by originating customer ID. |
| `shipping_last_name` | query | `string` | no | Filter by shipping last name. |
| `get_order_history` | query | `boolean` | no | Set to true to include order history in results. |
| `order_by` | query | `string` | no | Order field to sort by. Defaults to date_added. |
| `order` | query | `string` | no | Sort direction, ASC or DESC. |
