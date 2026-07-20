# Update Fuel Entry with Fleetio

Updates an existing fuel entry in Fleetio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `fuel_entries/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Update Fuel Entry](https://developer.fleetio.com/docs/api/fuel-entries-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the relevant record |
| `vehicle_id` | body | `number` | no | — |
| `vendor_id` | body | `number` | no | The Fleetio `id` of the [Vendor](/docs/api/vendors) associated with this Fuel Entry. |
| `fuel_type_id` | body | `number` | no | The Fleetio `id` of the [Fuel Type](/docs/api/fuel-types) associated with this Fuel Entry. |
| `date` | body | `date` | no | We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `us_gallons` | body | `number` | no | The fuel volume amount in US gallons. This field will _only_ be used if the [Vehicle](/docs/api/vehicles) is [configured to use US gallons](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings), otherwise it will be ignored. |
| `uk_gallons` | body | `number` | no | The fuel volume amount in UK gallons. This field will _only_ be used if the [Vehicle](/docs/api/vehicles) is [configured to use UK gallons](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings), otherwise it will be ignored. |
| `liters` | body | `number` | no | The fuel volume amount in liters. This field will be used if the [Vehicle](/docs/api/vehicles) is [configured to use liters](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings). |
| `price_per_volume_unit` | body | `number` | no | The unit price for the Vehicle's [configured volume unit](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings). |
| `meter_entry_attributes` | body | `object` | no | Each Fuel Entry requires an associated [Meter Entry](/docs/api/meter-entries) |
| `reference` | body | `string` | no | A reference number or identifier for this Fuel Entry. This field is often used to store a receipt number or other unique identifier. |
| `partial` | body | `boolean` | no | Indicates whether this Fuel Entry is a partial fill-up. Partial fill-ups are used to record Fuel Entries that are not full fill-ups. This field is `false` if not provided. |
| `personal` | body | `boolean` | no | Indicates whether this Fuel Entry is personal. Personal Fuel Entries are used to record fuel purchases that are not associated with a specific Vehicle or Equipment. This field is `false` if not provided. |
| `custom_fields` | body | `object` | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `documents_attributes` | body | `array<object>` | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `images_attributes` | body | `array<object>` | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
