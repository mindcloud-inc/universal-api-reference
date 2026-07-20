# Create Sales Order with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `sales_orders/create`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Create Sales Order](https://test-sku-mindcloud-api.wavelength.host/documentation/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order.addresses[].type` | body | `string` | no |
| `order.custom_fields[].name` | body | `string` | no |
| `order.instructions[].instructionId` | body | `number` | no |
| `order.order_lines[].child_lines[].custom_fields[].name` | body | `string` | no |
| `order.order_lines[].child_lines[].lineNumber` | body | `number` | no |
| `order.order_lines[].custom_fields[].name` | body | `string` | no |
| `order.order_lines[].line_number` | body | `number` | no |
| `order.shipments[].bill_of_lading` | body | `string` | no |
| `owner` | body | `string` | no |
| `order.addresses[].name` | body | `string` | no |
| `order.custom_fields[].value` | body | `string` | no |
| `order.instructions[].is_enabled` | body | `boolean` | no |
| `order.order_lines[].child_lines[].custom_fields[].value` | body | `string` | no |
| `order.order_lines[].child_lines[].material` | body | `string` | no |
| `order.order_lines[].custom_fields[].value` | body | `string` | no |
| `order.order_lines[].material` | body | `string` | no |
| `order.shipments[].booking_number` | body | `string` | no |
| `project` | body | `string` | no |
| `order_class` | body | `string` | no |
| `order.addresses[].reference` | body | `string` | no |
| `order.instructions[].entity_name` | body | `string` | no |
| `order.order_lines[].child_lines[].vendor_lot` | body | `string` | no |
| `order.order_lines[].vendor_lot` | body | `string` | no |
| `order.shipments[].lookup` | body | `string` | no |
| `order.addresses[].attention_of` | body | `string` | no |
| `order.instructions[].entity_keys` | body | `string` | no |
| `order.order_lines[].child_lines[].lot` | body | `string` | no |
| `order.order_lines[].lot` | body | `string` | no |
| `order.owner_reference` | body | `string` | no |
| `order.shipments[].expected_warehouse` | body | `string` | no |
| `order.addresses[].line_1` | body | `string` | no |
| `order.instructions[].type` | body | `string` | no |
| `order.order_lines[].child_lines[].packaging` | body | `string` | no |
| `order.order_lines[].packaging` | body | `string` | no |
| `order.shipments[].back_order` | body | `boolean` | no |
| `vendor_reference` | body | `string` | no |
| `order.addresses[].line_2` | body | `string` | no |
| `order.instructions[].created_on` | body | `string` | no |
| `order.order_lines[].child_lines[].packagedAmount` | body | `number` | no |
| `order.order_lines[].packaged_amount` | body | `number` | no |
| `requested_delivery_date` | body | `string` | no |
| `order.addresses[].city` | body | `string` | no |
| `order.instructions[].created_by` | body | `string` | no |
| `order.order_lines[].child_lines[].upc` | body | `string` | no |
| `order.order_lines[].upc` | body | `string` | no |
| `warehouse` | body | `string` | no |
| `carrier` | body | `string` | no |
| `order.addresses[].state` | body | `string` | no |
| `order.instructions[].modified_on` | body | `string` | no |
| `order.order_lines[].child_lines[]` | body | `array` | no |
| `order.order_lines[].child_lines[].custom_fields[]` | body | `array<object>` | no |
| `order.addresses[].postal_code` | body | `string` | no |
| `order.carrier_service` | body | `string` | no |
| `order.instructions[].modified_by` | body | `string` | no |
| `order.order_lines[].child_lines[].cost` | body | `number` | no |
| `order.order_lines[].custom_fields[]` | body | `array` | no |
| `addresses` | body | `array<object>` | no |
| `order.addresses[].country` | body | `string` | no |
| `order.instructions[].instruction` | body | `string` | no |
| `order.order_lines[].child_lines[].price` | body | `string` | no |
| `order.order_lines[].order_id` | body | `number` | no |
| `order_lines` | body | `array<object>` | no |
| `order.addresses[].lookup` | body | `string` | no |
| `order.order_lines[].cost` | body | `number` | no |
| `custom_fields` | body | `array<object>` | no |
| `order.addresses[].phone` | body | `string` | no |
| `order.order_lines[].price` | body | `number` | no |
| `order.addresses[].email` | body | `string` | no |
| `shipments` | body | `array<object>` | no |
| `lookup` | body | `string` | no |
| `order.addresses[].fax` | body | `string` | no |
| `instructions` | body | `array<object>` | no |
| `order.addresses[].title` | body | `string` | no |
| `currency` | body | `string` | no |
| `order.addresses[].greeting` | body | `string` | no |
| `notes` | body | `string` | no |
| `order.addresses[].first_name` | body | `string` | no |
| `order.addresses[].middle_name` | body | `string` | no |
| `order.project_id` | body | `string` | no |
| `order` | body | `object` | no |
| `order.addresses[].last_name` | body | `string` | no |
| `order.addresses[].is_residential` | body | `boolean` | no |
| `order.addresses[].notes` | body | `string` | no |
| `order.addresses[].order_id` | body | `number` | no |
