# Create Pickup with Easyship

Creates a new pickup in Easyship.

## Endpoint

- **Method:** `POST`
- **Path:** `/pickups`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Create Pickup](https://developers.easyship.com/reference/pickups_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courier_service_id` | body | `string` | yes | The unique identifier for the courier service. |
| `time_slot_id` | body | `string` | no | Pickup time slot ID. |
| `selected_date` | body | `string` | yes | Selected date for pickup. |
| `selected_from_time` | body | `string` | no | Selected pickup start time. |
| `selected_to_time` | body | `string` | no | Selected pickup end time. |
| `easyship_shipment_ids[]` | body | `array<string>` | yes | Shipment IDs to include in the pickup request. |
