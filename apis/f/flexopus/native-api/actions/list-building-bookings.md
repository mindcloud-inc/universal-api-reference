# List Building Bookings with Flexopus

Retrieves bookings for a specific Flexopus building.

## Endpoint

- **Method:** `GET`
- **Path:** `/buildings/:building_id/bookings`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Building Bookings](https://flexopus.com/api/docs/#endpoints-GETapi-v1-buildings--building_id--bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `building_id` | path | `number` | yes | The ID of the building. |
| `from` | query | `date` | yes | The start of the booking window as an ISO timestamp. |
| `to` | query | `date` | yes | The end of the booking window as an ISO timestamp. |
