# List Location Bookings with Flexopus

Retrieves bookings for a specific Flexopus location.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/:location_id/bookings`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Location Bookings](https://flexopus.com/api/docs/#endpoints-GETapi-v1-locations--location_id--bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | path | `number` | yes | The ID of the location. |
| `from` | query | `date` | yes | The start of the booking window as an ISO timestamp. |
| `to` | query | `date` | yes | The end of the booking window as an ISO timestamp. |
