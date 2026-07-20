# List Bookable Bookings with Flexopus

Retrieves bookings for a specific Flexopus bookable.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookables/:bookable_id/bookings`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Bookable Bookings](https://flexopus.com/api/docs/#endpoints-GETapi-v1-bookables--bookable_id--bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookable_id` | path | `number` | yes | The ID of the bookable resource. |
| `from` | query | `date` | yes | The start of the booking window as an ISO timestamp. |
| `to` | query | `date` | yes | The end of the booking window as an ISO timestamp. |
