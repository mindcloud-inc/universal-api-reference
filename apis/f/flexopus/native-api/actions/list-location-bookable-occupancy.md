# List Location Bookable Occupancy with Flexopus

Retrieves bookable occupancy for a Flexopus location.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/:location_id/bookables/occupancy`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Location Bookable Occupancy](https://flexopus.com/api/docs/#endpoints-GETapi-v1-locations--location_id--bookables-occupancy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | path | `number` | yes | The ID of the location. |
| `details` | query | `boolean` | no | Include current and next booking details in the occupancy response. |
