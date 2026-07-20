# Create Service Entry with Fleetio

Creates a new service entry in Fleetio.

## Endpoint

- **Method:** `POST`
- **Path:** `service_entries`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Create Service Entry](https://developer.fleetio.com/docs/api/service-entries-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `completed_at` | body | `date` | yes | The date and time at which the Service Entry was completed. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `meterEntryAttributes.value` | body | `number` | yes | The actual number on the vehicle's primary meter. Use the current odometer or meter reading for the associated vehicle. |
| `meterEntryAttributes.void` | body | `boolean` | no | Set this to true only if Fleetio rejects the meter value as too high or too low and you intentionally want to bypass that validation. |
| `vehicle_id` | body | `number` | yes | — |
| `meter_entry_attributes` | body | `object` | yes | A Service Entry may be associated with a [Meter Entry](/docs/api/meter-entries) |
| `started_at` | body | `date` | no | The date and time at which the Service Entry was started. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `vehicle_vin` | body | `string` | no | The VIN of the `Vehicle` associated with this Service Entry. |
| `vendor_id` | body | `number` | no | — |
| `reference` | body | `string` | no | A reference number for this Service Entry. |
| `label_list` | body | `string` | no | A comma separated list of tags associated with this record. The only delimiter allowed is a comma (`,`). Please remove any commas from your labels before saving the record. |
| `general_notes` | body | `string` | no | Any general notes about this Service Entry. |
| `vmrs_repair_priority_class_id` | body | `number` | no | — |
| `custom_fields` | body | `object` | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `secondary_meter_entry_attributes` | body | `object` | no | A Service Entry may also be associated with a secondary [Meter Entry](/docs/api/meter-entries) |
| `service_entry_line_items_attributes[]` | body | `array<object>` | no | Send multiple values as a array. |
| `issue_ids[]` | body | `array<number>` | no | The IDs of any Issues associated with this Service Entry. Send multiple values as a array. |
| `service_task_ids[]` | body | `array<number>` | no | The IDs of any Service Tasks associated with this Service Entry. Send multiple values as a array. |
| `comments_attributes[]` | body | `array<object>` | no | Send multiple values as a array. |
| `documents_attributes[]` | body | `array<object>` | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. Send multiple values as a array. |
| `images_attributes[]` | body | `array<object>` | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. Send multiple values as a array. |
| `labor_subtotal` | body | `number` | no | The total cost of labor for this Service Entry. This is calculated by summing the `labor_cost` of each `Service Entry Line Item`. |
| `parts_subtotal` | body | `number` | no | The total cost of `Parts` for this Service Entry. This is calculated by summing the `parts_cost` of each `Service Entry Line Item`. |
| `subtotal` | body | `number` | no | The subtotal amount of this Service Entry before any discounts or taxes. This is calculated by summing the `subtotal` of each `Service Entry Line Item`. |
| `discount` | body | `number` | no | The total discount amount for this Service Entry. |
| `discount_percentage` | body | `number` | no | The total discount percentage for this Service Entry. |
| `discount_type` | body | `string` | no | The type of discount applied to this record. |
| `tax_1` | body | `number` | no | The first tax amount for this Service Entry. |
| `tax_1_percentage` | body | `number` | no | The first tax percentage for this Service Entry. |
| `tax_1_type` | body | `string` | no | The type of tax to apply to this record. |
| `tax_2` | body | `number` | no | The second tax amount for this Service Entry. |
| `tax_2_percentage` | body | `number` | no | The second tax percentage for this Service Entry. |
| `tax_2_type` | body | `string` | no | The type of tax to apply to this record. |
| `total_amount` | body | `number` | no | The grand total of this Service Entry. |
