# Update Work Order with Fleetio

Updates an existing work order in Fleetio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `work_orders/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Update Work Order](https://developer.fleetio.com/docs/api/work-orders-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the relevant record |
| `issued_at` | body | `date` | no | The date and time at which this Work Order was issued. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `started_at` | body | `date` | no | The date and time at which this Work Order was started. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `completed_at` | body | `date` | no | The date and time at which this Work Order was completed. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `work_order_status_id` | body | `number` | no | — |
| `invoice_number` | body | `string` | no | The number of the `Invoice` associated with this Work Order. |
| `vendor_id` | body | `number` | no | — |
| `vendor_name` | body | `string` | no | The name of the `Vendor` associated with this Work Order. |
| `vehicle_id` | body | `number` | no | — |
| `vehicle_name` | body | `string` | no | The name of the `Vehicle` associated with this Work Order. |
| `discount_type` | body | `string` | no | The type of discount applied to this Work Order. |
| `discount` | body | `number` | no | The discount amount in decimal currency units applied to this Work Order. |
| `discount_percentage` | body | `number` | no | The percentage of the discount applied to this Work Order. Used if `discount_type` is set to `percentage`. |
| `parts_markup_percentage` | body | `number` | no | The percentage of the parts markup applied to this Work Order. Used if `parts_markup_type` is set to `percentage`.  Note: Parts markup fields are only writiable for Premium tier Fleetio Plan. |
| `parts_markup_type` | body | `string` | no | The type of parts markup to apply to this record.  Note: Parts markup fields are only writiable for Premium tier Fleetio Plan. |
| `parts_markup` | body | `number` | no | The amount of the parts markup applied to this Work Order. Used if `parts_markup_type` is set to `fixed`.  Note: Parts markup fields are only writiable for Premium tier Fleetio Plan. |
| `labor_markup_percentage` | body | `number` | no | The percentage of the labor markup applied to this Work Order. Used if `labor_markup_type` is set to `percentage`.  Note: Labor markup fields are only writiable for Premium tier Fleetio Plan. |
| `labor_markup_type` | body | `string` | no | The type of labor markup to apply to this record.  Note: Labor markup fields are only writiable for Premium tier Fleetio Plan. |
| `labor_markup` | body | `number` | no | The amount of the labor markup applied to this Work Order. Used if `labor_markup_type` is set to `fixed`.  Note: Labor markup fields are only writiable for Premium tier Fleetio Plan. |
| `tax_1_percentage` | body | `number` | no | The percentage of the first tax applied to this Work Order. Used if `tax_1_type` is set to `percentage`. |
| `tax_1_type` | body | `string` | no | The type of tax to apply to this record. |
| `tax_1` | body | `number` | no | The amount of the first tax applied to this Work Order. Used if `tax_1_type` is set to `amount`. |
| `tax_2_percentage` | body | `number` | no | The percentage of the second tax applied to this Work Order. Used if `tax_2_type` is set to `percentage`. |
| `tax_2_type` | body | `string` | no | The type of tax to apply to this record. |
| `tax_2` | body | `number` | no | The amount of the second tax applied to this Work Order. Used if `tax_2_type` is set to `amount`. |
| `issued_by_id` | body | `number` | no | — |
| `contact_id` | body | `number` | no | — |
| `label_list` | body | `string` | no | A comma separated list of tags associated with this record. The only delimiter allowed is a comma (`,`). Please remove any commas from your labels before saving the record. |
| `purchase_order_number` | body | `string` | no | The number of the `Purchase Order` associated with this Work Order. |
| `description` | body | `string` | no | A description of this Work Order. |
| `number` | body | `number` | no | The number to be applied to this Work Order. Must be unique. |
| `meter_entry_attributes` | body | `object` | no | A Work Order may also be associated with a [Meter Entry](/docs/api/meter-entries). |
| `secondary_meter_entry_attributes` | body | `object` | no | A Work Order may also be associated with a secondary [Meter Entry](/docs/api/meter-entries). |
| `starting_meter_entry_attributes` | body | `object` | no | The meter reading at the start of this Work Order. |
| `ending_meter_entry_attributes` | body | `object` | no | The meter reading at the end of this Work Order. |
| `starting_secondary_meter_entry_attributes` | body | `object` | no | The secondary meter reading at the start of this Work Order. |
| `ending_secondary_meter_entry_attributes` | body | `object` | no | The secondary meter reading at the end of this Work Order. |
| `custom_fields` | body | `object` | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `ending_meter_same_as_start` | body | `boolean` | no | Use start meter for completion meter? |
| `vmrs_repair_priority_class_id` | body | `number` | no | — |
| `scheduled_at` | body | `date` | no | The date and time at which this Work Order is scheduled. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `expected_completed_at` | body | `date` | no | The date and time at which this Work Order is expected to be completed. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `comments_attributes` | body | `array<object>` | no | A list of `Comments` to be added to this Work Order. |
| `work_order_line_items_attributes` | body | `array<object>` | no | A list of `Work Order Line Items` to be added to this Work Order. |
| `work_order_sub_line_items_attributes` | body | `array<object>` | no | A list of `Work Order Sub Line Items` to be added to this Work Order. |
| `issue_ids` | body | `array<number>` | no | A list of `Issues` to be added to this Work Order. |
| `label_ids` | body | `array<number>` | no | A list of `Labels` to be added to this Work Order. |
| `documents_attributes` | body | `array<object>` | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `images_attributes` | body | `array<object>` | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
