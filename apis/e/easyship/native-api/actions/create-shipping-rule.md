# Create Shipping Rule with Easyship

Creates a new shipping rule in Easyship.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipping_rules`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Create Shipping Rule](https://developers.easyship.com/reference/shipping_rules_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Shipping rule name. |
| `description` | body | `string` | yes | Shipping rule description. |
| `recalculate_shipments` | body | `boolean` | no | Recalculate all shipments affected by this shipping rule. |
| `priority` | body | `number` | no | Smaller values represent higher priority. |
| `conditions[]` | body | `array<object>` | yes | Array of shipping rule conditions. |
| `conditions[].type` | body | `string` | yes | Condition discriminator type. |
| `conditions[].options` | body | `object` | no | Condition options object. |
| `conditions[].options.country_ids[]` | body | `array<number>` | no | Country IDs for match_country conditions. |
| `conditions[].options.category_ids[]` | body | `array<string>` | no | Category IDs for match_category conditions. |
| `conditions[].options.states[]` | body | `array<string>` | no | State codes for match_state conditions. |
| `conditions[].options.operator` | body | `string` | no | Operator used by zipcode, SKU, buyer courier, item count, price, or weight conditions. |
| `conditions[].options.zipcodes[]` | body | `array<string>` | no | Zipcodes for match_zipcode conditions. |
| `conditions[].options.shipment_items_sku` | body | `string` | no | Shipment item SKU for match_sku conditions. |
| `conditions[].options.platform_names[]` | body | `array<string>` | no | Platform names for match_platform_name conditions. |
| `conditions[].options.store_ids[]` | body | `array<string>` | no | Store IDs for match_store conditions. |
| `conditions[].options.buyer_selected_courier_name` | body | `string` | no | Buyer-selected courier name for match_buyer_selected_courier_name conditions. |
| `conditions[].options.shipment_items_count` | body | `number` | no | Shipment item count for match_items_count conditions. |
| `conditions[].options.value` | body | `number` | no | Numeric value for price-based conditions. |
| `conditions[].options.currency` | body | `string` | no | Currency for selling-price conditions. |
| `conditions[].options.total_actual_weight` | body | `number` | no | Total actual weight for match_weight conditions. |
| `conditions[].options.order_tag_list[]` | body | `array<string>` | no | Order tags for include_order_tag_name conditions. |
| `actions[]` | body | `array<object>` | yes | Array of shipping rule actions. |
| `actions[].type` | body | `string` | yes | Action discriminator type. |
| `actions[].options` | body | `object` | no | Action options object. |
| `actions[].options.never_courier_service_ids[]` | body | `array<string>` | no | Courier service IDs to exclude. |
| `actions[].options.preferred_courier_service_ids[]` | body | `array<string>` | no | Courier service IDs to prefer. |
| `actions[].options.incoterms` | body | `string` | no | Incoterms to force. |
| `actions[].options.sort_by` | body | `string` | no | Sorting mode for courier selection. |
| `actions[].options.insured` | body | `boolean` | no | Whether to force insurance. |
| `actions[].options.force_tracking_rating[]` | body | `array<number>` | no | Tracking ratings to force. |
| `actions[].options.never_package_ids[]` | body | `array<string>` | no | Package IDs to reject. |
| `actions[].options.set_as_residential` | body | `boolean` | no | Whether to force residential surcharge behavior. |
| `actions[].options.origin_address_id` | body | `string` | no | Origin address ID to force. |
| `actions[].options.force_automated_return_requested` | body | `boolean` | no | Whether to force automated returns. |
| `actions[].options.operator` | body | `string` | no | Operator for forced delivery time actions. |
| `actions[].options.value` | body | `number` | no | Value for forced delivery time actions. |
