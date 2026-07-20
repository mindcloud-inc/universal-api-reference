# Update Vehicle with Fleetio

Updates an existing vehicle in Fleetio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `vehicles/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Update Vehicle](https://developer.fleetio.com/docs/api/vehicles-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Fleetio ID of the relevant Vehicle.  You may also look up Vehicles by their VIN, license plate, or other external ID. See the guide on [External Vehicle Ids](/docs/guides/vehicles/external-vehicle-ids) for information on how to set this up. |
| `color` | body | `string` | no | The color of this Vehicle. |
| `fuel_type_id` | body | `number` | no | The ID of the `Fuel Type` associated with this Vehicle. |
| `fuel_volume_units` | body | `string` | no | — |
| `group_id` | body | `number` | no | — |
| `group_hierarchy` | body | `string` | no | A pipe delimited group hierarchy. Ex: "Level 1\|Level 2\|Level 3". Where Level 1 is the parent of Level 2, and 2 is the parent of 3. Any missing nodes in the hierarchy will be created. |
| `label_ids` | body | `array<number>` | no | The `label_id`(s) of any Labels to assign to this Vehicle. If you wish to keep any existing Labels, those IDs must be included in this array as well. |
| `license_plate` | body | `string` | no | The license plate number of this Vehicle. |
| `make` | body | `string` | no | The name of this Vehicle's manufacturer. |
| `meter_unit` | body | `string` | no | The measurement unit used for the Vehicle's primary, or secondary (if applicable), meter. |
| `model` | body | `string` | no | The name of the model of this Vehicle. |
| `name` | body | `string` | no | A name to assign to this Vehicle. Must be unique. |
| `ownership` | body | `string` | no | — |
| `registration_expiration_month` | body | `number` | no | The month in which this Vehicle's registration expires. |
| `registration_state` | body | `string` | no | The state, province, or territory in which this Vehicle is registered. |
| `secondary_meter` | body | `boolean` | no | Indicates whether or not this Vehicle has a secondary meter. |
| `secondary_meter_unit` | body | `string` | no | The measurement unit used for the Vehicle's primary, or secondary (if applicable), meter. |
| `system_of_measurement` | body | `string` | no | — |
| `trim` | body | `string` | no | The trim level of this Vehicle. |
| `vehicle_status_id` | body | `number` | no | — |
| `vehicle_type_id` | body | `number` | no | — |
| `vin` | body | `string` | no | The Vehicle Identification Number of this Vehicle. Must be unique. |
| `year` | body | `number` | no | This Vehicle's model year. |
| `linked_vehicle_ids` | body | `array<number>` | no | The `vehicle_id`(s) of any Vehicles to link to this Vehicle. |
| `purchase_detail_attributes` | body | `object` | no | — |
| `external_ids` | body | `object` | no | Any [External IDs](/docs/guides/vehicles/external-vehicle-ids) associated with this Vehicle. |
| `vehicle_status_name` | body | `string` | no | The name of the `Vehicle Status` associated with this Vehicle. |
| `vehicle_type_name` | body | `string` | no | The name of the `Vehicle Type` associated with this Vehicle. |
| `in_service_date` | body | `date` | no | The date on which this Vehicle was put into service. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `in_service_meter` | body | `number` | no | The meter value at which this Vehicle was put into service. |
| `estimated_service_months` | body | `number` | no | The estimated number of months this Vehicle will be in service. |
| `estimated_replacement_mileage` | body | `number` | no | The estimated number of miles before which this Vehicle will be replaced. |
| `estimated_resale_price` | body | `number` | no | The estimated resale price of this Vehicle. |
| `out_of_service_date` | body | `date` | no | The date on which this Vehicle was or will be retired. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `out_of_service_meter` | body | `number` | no | The meter value at which this Vehicle was or will be retired. |
| `specs_attributes` | body | `object` | no | — |
| `custom_fields` | body | `object` | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
