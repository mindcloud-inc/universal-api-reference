# Update Shipment with Easyship

Updates an existing shipment in Easyship.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/shipments/:shipment_id`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Update Shipment](https://developers.easyship.com/reference/shipments_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipment_id` | path | `string` | yes | The Easyship shipment ID. |
| `origin_address_id` | body | `string` | no | Existing Easyship origin address ID. Leave blank if you provide the origin address object instead. |
| `origin_address` | body | `object` | no | Origin address object. |
| `origin_address.line_1` | body | `string` | no | Origin address line 1. |
| `origin_address.line_2` | body | `string` | no | Origin address line 2. |
| `origin_address.city` | body | `string` | no | Origin city. |
| `origin_address.state` | body | `string` | no | Origin state or province. |
| `origin_address.postal_code` | body | `string` | no | Origin postal code. |
| `origin_address.country_alpha2` | body | `string` | no | Origin country code. |
| `origin_address.company_name` | body | `string` | no | Origin company name. |
| `origin_address.contact_name` | body | `string` | no | Origin contact name. |
| `origin_address.contact_email` | body | `string` | no | Origin contact email. |
| `origin_address.contact_phone` | body | `string` | no | Origin contact phone. |
| `destination_address` | body | `object` | no | Destination address object. |
| `destination_address.line_1` | body | `string` | no | Destination address line 1. |
| `destination_address.line_2` | body | `string` | no | Destination address line 2. |
| `destination_address.city` | body | `string` | no | Destination city. |
| `destination_address.state` | body | `string` | no | Destination state or province. |
| `destination_address.postal_code` | body | `string` | no | Destination postal code. |
| `destination_address.country_alpha2` | body | `string` | no | Destination country code. |
| `destination_address.company_name` | body | `string` | no | Destination company name. |
| `destination_address.contact_name` | body | `string` | no | Destination contact name. |
| `destination_address.contact_email` | body | `string` | no | Destination contact email. |
| `destination_address.contact_phone` | body | `string` | no | Destination contact phone. |
| `parcels[]` | body | `array<object>` | no | Shipment parcels array. |
| `parcels[].items[]` | body | `array<object>` | no | Items included in a parcel. |
| `parcels[].box` | body | `object` | no | Parcel box details. |
| `parcels[].box.slug` | body | `string` | no | Courier or custom box slug. |
| `parcels[].total_actual_weight` | body | `number` | no | Total parcel weight in kilograms. |
| `parcels[].box.length` | body | `number` | no | Parcel box length. |
| `parcels[].box.width` | body | `number` | no | Parcel box width. |
| `parcels[].box.height` | body | `number` | no | Parcel box height. |
| `parcels[].items[].description` | body | `string` | no | Description of the parcel item. |
| `parcels[].items[].category` | body | `string` | no | Item category name or slug. |
| `parcels[].items[].sku` | body | `string` | no | Parcel item SKU. |
| `parcels[].items[].hs_code` | body | `string` | no | Parcel item HS code. |
| `parcels[].items[].contains_battery_pi966` | body | `boolean` | no | Whether the item applies PI966. |
| `parcels[].items[].contains_battery_pi967` | body | `boolean` | no | Whether the item applies PI967. |
| `parcels[].items[].contains_liquids` | body | `boolean` | no | Whether the item contains liquids. |
| `parcels[].items[].origin_country_alpha2` | body | `string` | no | Item origin country. |
| `parcels[].items[].quantity` | body | `number` | no | Parcel item quantity. |
| `parcels[].items[].dimensions` | body | `object` | no | Parcel item dimensions object. |
| `parcels[].items[].dimensions.length` | body | `number` | no | Parcel item length. |
| `parcels[].items[].dimensions.width` | body | `number` | no | Parcel item width. |
| `parcels[].items[].dimensions.height` | body | `number` | no | Parcel item height. |
| `parcels[].items[].actual_weight` | body | `number` | no | Parcel item actual weight. |
| `parcels[].items[].declared_currency` | body | `string` | no | Parcel item declared currency. |
| `parcels[].items[].declared_customs_value` | body | `number` | no | Parcel item declared customs value. |
| `parcels[].items[].product` | body | `object` | no | Parcel product reference object. |
| `parcels[].items[].product.id` | body | `string` | no | Product ID for product-backed parcel items. |
| `parcels[].items[].product.sku` | body | `string` | no | Product SKU for product-backed parcel items. |
| `parcels[].items[].id` | body | `string` | no | Item ID for return shipments. |
