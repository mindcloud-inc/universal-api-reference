# List Bookings with Flexopus

Retrieves a list of bookings from Flexopus.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [List Bookings](https://flexopus.com/api/docs/#endpoints-GETapi-v1-bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | yes | The start of the booking window as an ISO timestamp. |
| `to` | query | `date` | yes | The end of the booking window as an ISO timestamp. |
