# Create Purchase with Nudgify

Creates purchase events in Nudgify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/purchases`
- **Base URL:** `https://app.nudgify.com`
- **Official documentation:** [Create Purchase](https://www.nudgify.com/docs/knowledge-base/api-purchase-nudges/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | One or more purchase events to send to Nudgify. |
| `orders[].order_id` | body | `number` | yes | Integer order identifier for the purchase. |
| `orders[].date` | body | `string` | yes | UTC timestamp in `Y-m-d H:i:s` format. |
| `orders[].email` | body | `string` | no | Email address tied to the purchase. |
| `orders[].first_name` | body | `string` | no | First name to show in the nudge. |
| `orders[].last_name` | body | `string` | no | Last name to show in the nudge. |
| `orders[].ip` | body | `string` | no | IP address used for location fallback. |
| `orders[].city` | body | `string` | no | City to show in the nudge. |
| `orders[].state` | body | `string` | no | State or region to show in the nudge. |
| `orders[].country` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `orders[].line_items[]` | body | `array<object>` | no | Optional line items attached to the purchase. |
| `orders[].line_items[].item_id` | body | `number` | no | Item identifier for a purchased line item. Runtime validation required this to be an integer. |
| `orders[].line_items[].item_variation_id` | body | `string` | no | Variation or SKU identifier for the line item. |
| `orders[].line_items[].item_name` | body | `string` | no | Display name of the purchased item. |
| `orders[].line_items[].item_link` | body | `string` | no | Product page URL for the purchased item. |
| `orders[].line_items[].image_url` | body | `string` | no | Image URL for the purchased item. |
